# Radius

## Objetivo

O sistema de Radius define o arredondamento dos componentes da interface.

No StudyFlow, cada componente possui um raio de borda apropriado à sua função, proporcionando uma interface moderna, agradável e consistente.

A estratégia é inspirada no Material Design 3, porém adaptada à identidade visual do StudyFlow.

---

# Filosofia

Componentes diferentes possuem funções diferentes.

O raio deve refletir essa diferença.

Botões transmitem ação.

Cards transmitem organização.

Dialogs transmitem destaque.

---

# Radius Scale

| Token | Valor |
|--------|--------|
| xs | 4px |
| sm | 8px |
| md | 12px |
| lg | 16px |
| xl | 24px |
| full | 9999px |

---

# Component Radius

## Button

Radius

12px

Token

--radius-md

---

## Input

Radius

12px

Token

--radius-md

---

## Select

Radius

12px

---

## TextArea

Radius

12px

---

## Card

Radius

16px

Token

--radius-lg

---

## Statistics Card

Radius

16px

---

## Deck Card

Radius

16px

---

## Dialog

Radius

24px

Token

--radius-xl

---

## Bottom Sheet

Radius

24px

(Apenas bordas superiores)

---

## Snackbar

Radius

12px

---

## FAB

Radius

16px

---

## Chip

Radius

9999px

Token

--radius-full

---

## Badge

Radius

9999px

---

## Avatar

Radius

50%

---

## Progress Bar

Radius

9999px

---

# CSS Tokens

--radius-xs: 4px;

--radius-sm: 8px;

--radius-md: 12px;

--radius-lg: 16px;

--radius-xl: 24px;

--radius-full: 9999px;

---

# Guidelines

Utilizar sempre os tokens definidos.

Nunca utilizar valores arbitrários.

Cada componente deve manter seu raio em todas as telas.

O Radius não deve ser utilizado para diferenciar estados.

Estados são representados por:

- Cor
- Borda
- Elevação
- Animação

Nunca por Radius.