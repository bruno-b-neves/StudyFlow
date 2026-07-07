# Grid

## Objetivo

O sistema de Grid define como os elementos são distribuídos horizontalmente na interface.

Ele garante alinhamento, consistência e responsividade em todas as telas do StudyFlow.

O projeto segue a filosofia Mobile First.

---

# Mobile First

Toda interface deve ser projetada inicialmente para dispositivos móveis.

As versões Tablet e Desktop são adaptações da versão Mobile.

Fluxo de desenvolvimento

Mobile

↓

Tablet

↓

Desktop

---

# Breakpoints

| Dispositivo | Largura |
|-------------|----------|
| Mobile | 0 – 575px |
| Small Tablet | 576 – 767px |
| Tablet | 768 – 991px |
| Desktop | 992 – 1199px |
| Large Desktop | ≥1200px |

---

# Container

Mobile

100%

Padding horizontal

16px

Tablet

720px

Desktop

960px

Large Desktop

1140px

---

# Columns

Mobile

4 colunas

Tablet

8 colunas

Desktop

12 colunas

---

# Gutter

Espaçamento entre colunas

16px

Nunca alterar.

---

# Margins

Mobile

16px

Tablet

24px

Desktop

32px

---

# Layout Rules

Todos os componentes devem respeitar a Grid.

Nunca posicionar elementos manualmente.

Evitar larguras fixas.

Sempre utilizar:

- width: 100%
- max-width

---

# Component Width

Inputs

100%

Buttons

100% (Mobile)

Auto (Desktop quando necessário)

Cards

100%

Dialogs

Máximo 480px

---

# Alignment

O alinhamento padrão do sistema é:

Horizontal

Left

Vertical

Top

Exceções

- Login
- Register
- Empty States
- Study Summary

Nessas telas o conteúdo pode ser centralizado.

---

# Responsive Behavior

Mobile

Empilhamento vertical.

Tablet

Duas colunas quando fizer sentido.

Desktop

Até três colunas.

Nunca comprometer a leitura.

---

# Bootstrap Integration

O StudyFlow utiliza a Grid do Bootstrap como infraestrutura.

Exemplo

container

↓

row

↓

col

Entretanto, a organização visual seguirá as regras definidas neste documento.

---

# Guidelines

Evitar posicionamentos absolutos.

Priorizar Flexbox.

Utilizar Grid apenas quando houver benefício claro.

O usuário nunca deve precisar realizar scroll horizontal.

---

# Example

Dashboard

Container

↓

Header

↓

Statistics

↓

Deck List

↓

FAB

Todos alinhados respeitando a Grid.