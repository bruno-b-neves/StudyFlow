# ADR-003 - Estratégia de Repetição Espaçada (Spaced Repetition Strategy)

- **Status:** Aceito
- **Data:** 03/07/2026
- **Autor:** Bruno Neves

---

## Contexto

O principal objetivo do StudyFlow é auxiliar usuários na memorização de conteúdos utilizando repetição espaçada.

Durante o desenvolvimento do domínio surgiu a necessidade de definir como o sistema reagirá às respostas fornecidas pelo usuário durante uma revisão.

Cada resposta deverá atualizar o estado de aprendizagem do Flashcard e determinar quando ele será apresentado novamente.

---

## Problema

Como calcular os próximos intervalos de revisão de forma eficiente, simples para a primeira versão e preparada para futuras evoluções?

---

## Decisão

A primeira versão do StudyFlow utilizará um algoritmo inspirado no SM-2, amplamente utilizado por sistemas de repetição espaçada.

Entretanto, a implementação será própria e organizada de forma que possa ser personalizada pelo usuário e evoluída futuramente com suporte à Inteligência Artificial.

---

## Estados de Aprendizagem

Todo CardProgress poderá estar em um dos seguintes estados:

- NEW
- LEARNING
- REVIEW
- MASTERED

Cada estado determina o comportamento do algoritmo de revisão.

---

## Comportamento das Respostas

### Again

Representa que o usuário não conseguiu recordar o conteúdo.

O sistema deverá:

- Permanecer no estado LEARNING.
- Incrementar o contador de lapses.
- Reagendar o Flashcard para reaparecer ainda na sessão atual.
- Utilizar um intervalo curto configurável (30 segundos por padrão).

---

### Hard

Representa que o usuário conseguiu lembrar com dificuldade.

O sistema deverá:

- Permanecer no estado atual.
- Aplicar um pequeno aumento no intervalo.
- Reduzir levemente o Ease Factor.

---

### Good

Representa uma resposta considerada satisfatória.

O sistema deverá:

- Registrar uma revisão bem-sucedida.
- Incrementar o contador de repetições.
- Calcular o próximo intervalo normalmente.

---

### Easy

Representa que o usuário respondeu facilmente.

O sistema deverá:

- Registrar uma revisão bem-sucedida.
- Incrementar as repetições.
- Aumentar o Ease Factor.
- Aplicar um intervalo maior que o padrão.

---

## Configurações

Os usuários poderão personalizar futuramente:

- Intervalo do Again
- Intervalo inicial
- Ease Factor inicial
- Limite máximo de intervalo
- Multiplicadores de crescimento

Na V1 serão utilizados valores padrão.

---

## Objetivos

A estratégia adotada busca:

- Maximizar retenção de memória.
- Reduzir revisões desnecessárias.
- Permitir evolução futura.
- Manter simplicidade na implementação inicial.

---

## Consequências

### Positivas

- Algoritmo desacoplado da interface.
- Fácil manutenção.
- Preparação para IA.
- Configurações futuras sem alterar o domínio.

### Negativas

- Necessidade de calibração dos parâmetros.
- Evolução gradual do algoritmo ao longo das versões.

---

## Impacto no Domínio

Entidades afetadas:

- CardProgress
- Review
- StudySession

Serviços de domínio:

- ReviewEngine

Eventos relacionados:

- CardReviewed
- CardProgressUpdated
- NextReviewScheduled

---

## Decisões futuras relacionadas

Versões futuras poderão incluir:

- Aprendizado adaptativo baseado em IA.
- Ajuste automático do Ease Factor.
- Análise individual de desempenho.
- Recomendações inteligentes.
- Estratégias diferentes por idioma.
- Algoritmos alternativos (FSRS).

---

## Status da implementação

- [x] Decisão arquitetural aprovada.
- [ ] Modelagem do domínio.
- [ ] Implementação do ReviewEngine.
- [ ] Backend.
- [ ] Frontend.