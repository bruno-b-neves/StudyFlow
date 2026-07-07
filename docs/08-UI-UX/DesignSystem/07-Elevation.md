# Elevation

## Objetivo

O sistema de elevação define como os componentes se destacam visualmente na interface.

No StudyFlow, a elevação é utilizada de forma discreta.

O objetivo é criar profundidade sem competir com o conteúdo.

---

# Filosofia

O aprendizado deve ser o protagonista.

A interface deve transmitir calma e organização.

Por isso, o uso de sombras será mínimo.

Sempre que possível, utilizar:

- Espaçamento
- Bordas
- Contraste

Antes de utilizar sombras.

---

# Elevation Levels

## Level 0

Nenhuma sombra.

Uso

- Background
- Layout

Shadow

none

---

## Level 1

Elevação mínima.

Uso

- Cards
- Inputs
- Bottom Navigation

Shadow

0 1px 2px rgba(15, 23, 42, 0.08)

---

## Level 2

Elevação média.

Uso

- FAB
- Dropdown
- Menu

Shadow

0 4px 8px rgba(15, 23, 42, 0.12)

---

## Level 3

Elevação alta.

Uso

- Dialog
- Modal
- Bottom Sheet

Shadow

0 8px 24px rgba(15, 23, 42, 0.16)

---

# Border Strategy

Sempre que possível utilizar bordas antes de sombras.

Border

1px solid var(--color-border)

Exemplos

Cards

Inputs

Dialogs

---

# Hover

Durante Hover

Aumentar apenas um nível.

Exemplo

Card

Level 1

↓

Hover

Level 2

---

# Dark Theme

No modo escuro as sombras devem ser reduzidas.

O contraste entre superfícies será o principal mecanismo de profundidade.

---

# Tokens

--shadow-none

--shadow-sm

--shadow-md

--shadow-lg

---

# CSS Tokens

--shadow-none: none;

--shadow-sm:
0 1px 2px rgba(15,23,42,.08);

--shadow-md:
0 4px 8px rgba(15,23,42,.12);

--shadow-lg:
0 8px 24px rgba(15,23,42,.16);

---

# Guidelines

Nunca utilizar sombras excessivas.

Evitar múltiplas sombras no mesmo componente.

A profundidade deve ser percebida de forma natural.

O conteúdo sempre deve chamar mais atenção que a interface.