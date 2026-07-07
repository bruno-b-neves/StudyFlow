# Motion

## Objetivo

O sistema de Motion define como a interface responde às ações do usuário através de animações e transições.

No StudyFlow, as animações possuem um único propósito:

Melhorar a experiência de aprendizagem.

Nenhuma animação deve existir apenas por motivos estéticos.

---

# Filosofia

Motion deve comunicar.

Nunca distrair.

As animações devem:

- Guiar o usuário
- Confirmar ações
- Indicar mudanças de estado
- Tornar a interface mais natural

---

# Princípios

## Natural

As animações devem parecer leves.

Nunca rápidas demais.

Nunca lentas.

---

## Funcional

Toda animação precisa possuir um objetivo.

Exemplos

✔ Mostrar progresso

✔ Confirmar salvamento

✔ Revelar resposta

✔ Abrir Dialog

---

## Discreta

Evitar exageros.

Nada deve competir com o conteúdo estudado.

---

# Duração

Fast

150ms

Uso

Hover

Focus

Botões

---

Medium

250ms

Uso

Cards

Dialogs

Snackbars

---

Slow

350ms

Uso

Troca de páginas

Study Session

---

# Easing

Padrão

ease-out

Entradas

ease-out

Saídas

ease-in

Elementos complexos

ease-in-out

---

# Animações Permitidas

## Fade

Uso

Snackbars

Dialogs

Mensagens

---

## Slide

Uso

Bottom Sheet

Drawer

Menus

---

## Scale

Uso

FAB

Botões

Feedback

---

## Flip

Uso

Flashcards

Mostrar resposta

Ocultar resposta

---

## Progress

Uso

Barra de progresso

Estudo

Upload

---

## Skeleton

Uso

Loading

Dashboard

Decks

Flashcards

---

# Feedback Visual

Salvar Flashcard

✓ Snackbar

↓

Fade

---

Criar Deck

✓ Snackbar

↓

Fade

---

Excluir Deck

Dialog

↓

Fade

↓

Scale

---

# Study Session

Durante o estudo

Mostrar Resposta

↓

Flip Animation

↓

Botões Again Hard Good Easy

↓

Fade In

---

Próximo Flashcard

↓

Slide Horizontal

↓

Novo Card

---

Fim da Sessão

↓

Confetti (Muito discreto)

↓

Summary

---

# Hover

Desktop

Scale 1.02

Shadow +1

---

Mobile

Sem Hover

---

# Loading

Utilizar Skeleton Loading.

Evitar Spinners longos.

---

# Accessibility

Respeitar usuários com redução de movimento.

Se o sistema operacional possuir

prefers-reduced-motion

↓

Desabilitar animações não essenciais.

---

# Tokens

--duration-fast

--duration-medium

--duration-slow

--ease-default

--ease-enter

--ease-exit

---

# CSS Tokens

--duration-fast: 150ms;

--duration-medium: 250ms;

--duration-slow: 350ms;

--ease-default: ease-out;

--ease-enter: ease-out;

--ease-exit: ease-in;

--ease-standard: ease-in-out;

---

# Guidelines

Nunca utilizar animações apenas para decorar.

Toda animação deve comunicar uma mudança de estado.

O conteúdo estudado sempre deve permanecer como foco principal.