# Spacing

## Objetivo

O sistema de espaçamento define a distância entre todos os elementos da interface.

Seu objetivo é criar consistência visual, facilitar a leitura e reduzir a carga cognitiva durante o uso do StudyFlow.

O Design System utiliza uma escala baseada em múltiplos de 4 pixels.

---

# Base Unit

4px

Toda distância da interface deve ser um múltiplo desta unidade.

Nunca utilizar valores arbitrários.

Exemplos incorretos:

- 7px
- 11px
- 13px
- 19px

---

# Spacing Scale

| Token | Valor |
|-------|-------|
| xs | 4px |
| sm | 8px |
| md | 12px |
| lg | 16px |
| xl | 24px |
| 2xl | 32px |
| 3xl | 48px |
| 4xl | 64px |
| 5xl | 96px |

---

# Uso recomendado

4px

Pequenos ajustes.

Exemplo:

Ícone → Texto

---

8px

Espaçamento interno de pequenos componentes.

Exemplo:

Botões

Chips

Badges

---

12px

Espaçamento entre Label e Input.

Exemplo:

E-mail

[____________]

---

16px

Espaçamento padrão.

Utilizado em:

- Cards
- Inputs
- Botões
- Listas

---

24px

Separação entre seções.

Exemplo:

Estatísticas

↓

Meus Decks

---

32px

Separação entre grandes blocos.

Exemplo:

Header

↓

Conteúdo

---

48px

Grandes áreas da interface.

Exemplo:

Landing Pages

Empty States

---

64px

Espaços especiais.

Utilizar apenas quando realmente necessário.

---

# Padding

Botões

Vertical

12px

Horizontal

16px

---

Inputs

Vertical

12px

Horizontal

16px

---

Cards

16px

---

Dialogs

24px

---

# Margin

Entre Cards

16px

Entre Seções

24px

Entre Tela e Conteúdo

16px

Entre Botões

8px

---

# Layout

Padding horizontal padrão

16px

Padding vertical padrão

16px

---

# Guidelines

Sempre reutilizar os tokens.

Nunca utilizar valores fixos diretamente nos componentes.

Exemplo

Correto

padding: var(--spacing-lg);

Incorreto

padding: 17px;

---

# Responsividade

O sistema de espaçamento permanece consistente entre:

- Mobile
- Tablet
- Desktop

O que muda é apenas a largura disponível.

Nunca a escala.