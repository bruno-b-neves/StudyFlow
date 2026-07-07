# Deck

## Objetivo

A tela de Decks permite que o usuário organize seus estudos através de coleções de Flashcards.

Cada Deck representa um assunto específico de estudo.

Exemplos:

- Inglês
- Espanhol
- Japonês
- Verbos Irregulares
- TOEFL
- IELTS

O objetivo desta tela é oferecer uma organização simples, intuitiva e escalável para qualquer quantidade de Decks.

---

# Público

Usuários autenticados.

---

# Objetivos de UX

- Facilitar a organização do estudo.
- Localizar rapidamente um Deck.
- Incentivar a criação de novos Decks.
- Permitir acesso rápido aos Flashcards.
- Evitar poluição visual mesmo com muitos Decks.

---

# Objetivos de Negócio

- Incentivar criação de novos conteúdos.
- Melhorar organização dos estudos.
- Aumentar frequência de revisões.
- Preparar integração futura com IA.

---

# Estrutura da Página

A página será composta por:

1. Header
2. Barra de pesquisa
3. Filtros
4. Lista de Decks
5. Botão Criar Deck
6. Paginação (caso necessário)

---

# Header

Componentes

- Breadcrumb
- Título
- Botão Criar Deck

Título

Meus Decks

---

# Barra de Pesquisa

Permite localizar Decks rapidamente.

Placeholder

Pesquisar Deck...

Pesquisa em

- Nome
- Descrição

A pesquisa será instantânea.

---

# Filtros

Filtros disponíveis

Todos

Recentes

Arquivados

Favoritos (V2)

Idioma

Quantidade de Flashcards

---

# Lista de Decks

Cada Deck será apresentado em formato de Card.

Cada Card deverá exibir:

Nome

Descrição

Idioma

Quantidade de Flashcards

Flashcards pendentes

Último estudo

Data de criação

Status

---

# Exemplo

🇺🇸 Inglês

Aprendizado geral.

320 Flashcards

23 pendentes

Último estudo

Hoje às 08:15

Criado em

15/06/2026

Status

Ativo

---

# Ações do Deck

Abrir

Editar

Duplicar (V2)

Arquivar

Excluir

Exportar (V2)

Compartilhar (V2)

---

# Criar Deck

Botão

Novo Deck

Ao clicar:

Abrirá Modal.

Campos

Nome

Descrição

Idioma

Imagem (V2)

Cor (V2)

Botões

Cancelar

Criar

---

# Editar Deck

Permite alterar

Nome

Descrição

Idioma

---

# Excluir Deck

Antes da exclusão será apresentada confirmação.

Mensagem

Deseja realmente excluir este Deck?

Esta ação não poderá ser desfeita.

Botões

Cancelar

Excluir

---

# Arquivar Deck

Decks arquivados

Não aparecem no Dashboard.

Continuam disponíveis para restauração.

Nenhum dado será perdido.

---

# Estado Vazio

Mensagem

Você ainda não criou nenhum Deck.

Botão

Criar meu primeiro Deck.

Ilustração amigável.

---

# Estado de Carregamento

Skeleton para:

Cards

Pesquisa

Filtros

---

# Estado de Erro

Mensagem

Não foi possível carregar seus Decks.

Botão

Tentar novamente.

---

# Componentes Utilizados

Header

SearchInput

FilterDropdown

DeckCard

PrimaryButton

Modal

EmptyState

SkeletonCard

ErrorState

ConfirmationDialog

---

# Navegação

Dashboard

↓

Deck

↓

Flashcards

↓

Study Session

---

# Regras de Negócio

Cada Deck pertence exclusivamente a um usuário.

Um Deck pode existir vazio.

Um Deck pode conter milhares de Flashcards.

Um Deck arquivado não participa das sessões de estudo.

Decks excluídos terão seus Flashcards removidos.

---

# Permissões

Usuário autenticado

Pode criar Deck.

Pode editar apenas seus próprios Decks.

Pode excluir apenas seus próprios Decks.

Não pode visualizar Decks de outros usuários.

---

# Performance

Pesquisa com debounce.

Paginação automática.

Lazy Loading para listas grandes.

---

# Responsividade

## Desktop

Grid com múltiplos Cards.

## Tablet

Grid reduzido.

## Mobile

Cards em coluna única.

Botão Novo Deck sempre visível.

---

# Acessibilidade

Navegação por teclado.

Contraste WCAG AA.

Leitores de tela.

Labels em todos os campos.

---

# Eventos

Deck Created

Deck Opened

Deck Edited

Deck Archived

Deck Deleted

Search Performed

---

# Métricas

Quantidade de Decks criados.

Decks ativos.

Decks arquivados.

Quantidade média de Flashcards por Deck.

Tempo médio até criar primeiro Deck.

---

# Futuras Versões

Categorias.

Favoritos.

Compartilhamento.

Templates.

Decks públicos.

Decks gerados por IA.

Importação automática de PDFs.

Importação de vídeos.

Importação de legendas.

---

# Critérios de Aceitação

- Usuário pode criar um Deck.
- Usuário pode editar um Deck.
- Usuário pode excluir um Deck.
- Usuário pode arquivar um Deck.
- Pesquisa funciona em tempo real.
- Layout responsivo.
- Estado vazio implementado.
- Skeleton Loading implementado.