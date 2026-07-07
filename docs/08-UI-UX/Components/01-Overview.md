# Component Library

## Objetivo

A Component Library do StudyFlow reúne todos os componentes reutilizáveis utilizados na aplicação.

Seu objetivo é garantir consistência visual, facilitar a manutenção e acelerar o desenvolvimento de novas funcionalidades.

Todos os componentes devem seguir os Foundations definidos no Design System.

---

# Filosofia

A interface do StudyFlow é construída através da composição de componentes.

Nenhuma tela deve criar elementos visuais diretamente.

Toda interface deve ser composta por componentes reutilizáveis.

Exemplo

Dashboard

↓

TopAppBar

↓

StatisticsCard

↓

DeckCard

↓

BottomNavigation

---

# Hierarquia

Os componentes são divididos em três níveis.

---

## Base Components

São componentes genéricos.

Não possuem conhecimento do domínio.

Exemplos

BaseButton

BaseInput

BaseCard

BaseDialog

BaseSnackbar

BaseAvatar

BaseIcon

BaseProgress

BaseChip

BaseBadge

---

## Composite Components

São compostos por Base Components.

Já representam partes do domínio.

Exemplos

DeckCard

FlashcardCard

StatisticsCard

StudyProgress

SearchBar

ProfileHeader

TopAppBar

BottomNavigation

---

## Page Components

São responsáveis por montar uma tela.

Não devem conter regras de negócio.

Exemplos

Dashboard

Deck Details

Create Flashcard

Study Session

Study Summary

Profile

Settings

---

# Responsabilidades

Base Components

↓

Aparência

Estados

Acessibilidade

---

Composite Components

↓

Composição

Layout

Experiência

---

Pages

↓

Organização

Fluxo

Navegação

---

# Reutilização

Antes de criar um novo componente, verificar:

O componente já existe?

Pode ser reutilizado?

Pode ser estendido?

Evitar duplicação.

---

# Estados

Todo componente interativo deve possuir:

Default

Hover

Focused

Pressed

Disabled

Loading

Error

Success

Quando aplicável.

---

# Acessibilidade

Todo componente deve:

Possuir navegação por teclado.

Possuir aria-label quando necessário.

Possuir contraste adequado.

Possuir estados de foco.

Ser utilizável por leitores de tela.

---

# Composição

Componentes maiores devem ser construídos apenas utilizando componentes menores.

Exemplo

DeckCard

↓

BaseCard

↓

BaseButton

↓

BaseIcon

↓

Typography

---

# Responsabilidade Única

Cada componente deve possuir apenas uma responsabilidade.

Exemplo

BaseButton

↓

Renderizar um botão.

Não realizar chamadas HTTP.

Não acessar Store.

Não conhecer regras de negócio.

---

# Dependências

Os componentes nunca devem depender diretamente:

do Backend

do Banco de Dados

do Spring Boot

Eles devem depender apenas de:

Props

Slots

Eventos

---

# Comunicação

A comunicação entre componentes deve ocorrer através de:

Props

Eventos

Slots

Nunca através de acesso direto a componentes filhos.

---

# Convenções

Todos os componentes Vue utilizarão:

PascalCase

Exemplos

BaseButton.vue

DeckCard.vue

StudyProgress.vue

BottomNavigation.vue

---

# Estrutura

components/

base/

BaseButton.vue

BaseInput.vue

BaseCard.vue

...

composite/

DeckCard.vue

StatisticsCard.vue

FlashcardCard.vue

...

layout/

TopAppBar.vue

BottomNavigation.vue

...

---

# Objetivo Final

Toda interface do StudyFlow deverá ser construída apenas reutilizando componentes existentes.

Sempre que possível, um novo componente deve nascer da composição de componentes já existentes.