# Modelagem do Domínio

## Visão Geral do Domínio

O StudyFlow é uma plataforma de aprendizado baseada em repetição espaçada (Spaced Repetition), voltada inicialmente para o estudo de idiomas. Seu objetivo é auxiliar usuários na memorização de conteúdos por meio de Flashcards organizados em Decks, registrando o progresso individual de aprendizagem e adaptando automaticamente as revisões conforme o desempenho do usuário.

## Linguagem Ubíqua

| Termo        | Definição                                                                     |
| ------------ | ----------------------------------------------------------------------------- |
| User         | Pessoa que utiliza a plataforma.                                              |
| Deck         | Coleção de Flashcards criada por um User.                                     |
| Flashcard    | Unidade de estudo composta por um conteúdo frontal e um conteúdo de resposta. |
| StudySession | Período em que um User realiza revisões.                                      |
| Review       | Registro da resposta dada pelo usuário durante uma revisão.                   |
| CardProgress | Estado de aprendizagem de um User para um Flashcard específico.               |


## Entidades

### User

O que é?

Representa uma pessoa cadastrada na plataforma.

Responsabilidade:
Ser a identidade principal do sistema.

Pode fazer:
* Criar Decks.
* Criar Flashcards.
* Estudar.
* Acompanhar seu progresso.

Não deve fazer:

* Calcular o algoritmo de repetição.
* Armazenar estatísticas de aprendizado.
* Controlar revisões.

### Deck

O que é um Deck?

Um Deck representa uma coleção organizada de Flashcards criada por um User para estudar um determinado assunto ou objetivo específico.

Qual é a responsabilidade do Deck?

* Organizar Flashcards.
* Representar um tema de estudo.
* Permitir ao usuário estruturar seu conhecimento.

O que ele pode fazer?

* Adicionar Flashcards.
* Remover Flashcards.
* Alterar sua ordem.
* Ser arquivado.
* Ser compartilhado futuramente (V2).
* Ser exportado futuramente.
* Alterar informações do Deck (nome, descrição, etc.).
* Excluir o Deck.

O que ele NÃO deve fazer?

* Não controla o progresso do usuário.
* Não calcula revisões.
* Não registra respostas.
* Não conhece o algoritmo de repetição.
* Não conhece o desempenho do usuário.
* Não decide qual Flashcard será exibido na próxima revisão.

Um Deck pode existir vazio?

Sim. Adicionar conteúdo faz parte do fluxo natural.
Um Deck pode existir sem Flashcards.

Regras de negócio:

* Um Deck pode existir vazio.
* Um Deck pertence a apenas um User.
* Um Deck pode conter zero ou muitos Flashcards.
* Um Flashcard pertence a apenas um Deck (na V1).
* Excluir um Deck implica excluir todos os seus Flashcards.

### Flashcard

Oque é?

Um Flashcard representa a menor unidade de aprendizado dentro de um Deck. Seu objetivo é apresentar uma informação ao usuário e avaliar sua capacidade de recordá-la.

Um Flashcard é responsável por:

* Representar um conteúdo de estudo.
* Permitir que o usuário pratique a memorização.
* Pertencer a um único Deck.
* Servir de base para o algoritmo de repetição.
  
O que ele pode fazer?
* Armazenar um conteúdo principal.
* Armazenar um conteúdo de resposta.
* Possuir mídia (V2).
* Possuir exemplos (V2).
* Possuir observações (V2).
* Ser editado.
* Ser removido.
  
O que ele NÃO deve fazer?

* Não sabe quando será revisado.
* Não conhece o progresso do usuário.
* Não calcula intervalos.
* Não registra respostas.
* Não conhece o Ease Factor.
* Não conhece o Ease Factor.

---

Regras de negócio

- Todo Flashcard pertence obrigatoriamente a um Deck.
- Um Flashcard não pode existir sem um Deck.
- Um Flashcard pode ser editado pelo proprietário do Deck.
- Excluir um Flashcard remove também seu progresso associado.

Invariantes

- Um Flashcard pertence a exatamente um Deck.
- Um Flashcard sempre representa uma unidade de aprendizado.
- Um Flashcard não armazena informações de progresso.
- Um Flashcard não conhece usuários.

### CardProgress

O que é?

O CardProgress representa o estado de aprendizagem de um User em relação a um Flashcard específico.

O CardProgress é responsável por:

* Registrar a evolução do aprendizado.
* Armazenar informações utilizadas pelo algoritmo de repetição.
* Determinar quando um Flashcard deverá ser revisado novamente.
* Representar o estado atual de aprendizagem daquele cartão para um usuário específico.

O que ele pode fazer?

* Atualizar seu estado após uma revisão.
* Registrar a próxima revisão.
* Registrar o histórico básico de evolução.
* Indicar se o Flashcard está em aprendizado, revisão ou domínio.

O que ele NÃO deve fazer?

* Não conhece o conteúdo do Flashcard.
* Não calcula o algoritmo.
* Não registra a resposta do usuário.
* Não inicia Study Sessions.
* Não pertence ao Deck.

Regras de negócio:

Ao reiniciar o aprendizado de um Deck, os registros de CardProgress ativos são arquivados e novos registros são criados conforme os Flashcards forem estudados novamente. O conteúdo do Deck permanece inalterado.

* Um User possui um CardProgress para cada Flashcard estudado.
* Um Flashcard pode possuir milhares de CardProgress. Cada usuário terá o seu.
* Um CardProgress só existe após o primeiro estudo.

---

Quais informações ele precisa conhecer?

| id   | user   | flashcard   | learningState | easeFactor   | interval   | repetitions   | lapses   | nextReview   | lastReviewedAt   | createdAt   | updatedAt   | archivedAt   |
| ---- |------- | ----------- | ------------- | ------------ | ---------- | ------------- | -------- | ------------ | ---------------- | ----------- | ----------- | ------------ |

### StudySession

### Review

## Relacionamentos

## Regras de Negócio

## Eventos do Domínio