# Design System

## Objetivo

O Design System do StudyFlow define todos os padrões visuais e de interação da plataforma.

Seu objetivo é garantir consistência entre todas as telas, reduzir retrabalho e facilitar a criação de novos componentes.

Este documento será a principal referência para Designers e Desenvolvedores.

---

# Princípios

Todo componente deve seguir estes princípios.

## Clareza

A interface deve comunicar imediatamente sua função.

Nunca exigir que o usuário "descubra" como usar.

---

## Consistência

Componentes semelhantes devem sempre possuir o mesmo comportamento.

---

## Simplicidade

Remover qualquer elemento que não agregue valor.

---

## Acessibilidade

Todo componente deve funcionar com:

- Mouse
- Teclado
- Touch
- Screen Readers

---

## Performance

Animações leves.

Componentes reutilizáveis.

Poucas dependências.

---

# Paleta de Cores

## Primary

Representa:

Aprendizado

Confiança

Tecnologia

Uso

Botões principais

Links

Ações principais

---

## Secondary

Representa

Organização

Apoio

Elementos secundários

---

## Success

Representa

Conclusão

Progresso

Acertos

---

## Warning

Representa

Atenção

Informações importantes

---

## Danger

Representa

Erros

Exclusões

Falhas

---

## Info

Representa

Mensagens informativas.

---

# Background

Teremos dois temas.

## Light

Fundo claro.

Cards brancos.

---

## Dark

Cinza muito escuro.

Nunca preto absoluto.

---

# Tipografia

## Família

Será utilizada uma fonte moderna, limpa e altamente legível.

Exemplos

Inter

Roboto

Nunito

---

# Escala

Display

Heading 1

Heading 2

Heading 3

Subtitle

Body

Small

Caption

---

# Peso

Regular

Medium

SemiBold

Bold

---

# Espaçamento

Toda interface utilizará uma escala fixa.

4

8

12

16

24

32

48

64

Nunca utilizar valores aleatórios.

---

# Border Radius

Small

4px

Medium

8px

Large

12px

Extra Large

16px

---

# Sombras

Shadow 1

Elementos discretos.

Shadow 2

Cards.

Shadow 3

Modais.

Shadow 4

Elementos elevados.

---

# Grid

Desktop

12 colunas.

Tablet

8 colunas.

Mobile

4 colunas.

---

# Breakpoints

Mobile

< 768px

Tablet

768px

Desktop

1024px

Large Desktop

1440px

---

# Ícones

Biblioteca

Lucide Icons.

Todos os ícones terão:

24x24

Stroke consistente.

---

# Botões

Tipos

Primary

Secondary

Outline

Ghost

Danger

---

# Estados

Default

Hover

Active

Disabled

Loading

Focus

---

# Inputs

Text

Password

Email

Search

Textarea

Select

Date

Upload

---

# Estados

Default

Focus

Disabled

Error

Success

Loading

---

# Cards

BaseCard

DeckCard

FlashcardCard

StatisticCard

StudyCard

AIRecommendationCard

---

# Modais

Small

Medium

Large

Fullscreen

---

# Badges

Success

Danger

Info

Warning

Primary

---

# Avatares

Small

Medium

Large

---

# Tabelas

Header fixo.

Hover nas linhas.

Responsivas.

---

# Feedback

Loading

Skeleton Loading

Nunca Spinner central.

---

Empty State

Ilustração.

Mensagem.

Botão principal.

---

Error State

Mensagem clara.

Botão tentar novamente.

---

Success State

Mensagem positiva.

Ícone.

---

# Navegação

Sidebar Desktop.

Bottom Navigation Mobile (V2).

Breadcrumb.

---

# Animações

Permitidas

Fade

Slide

Scale

Não permitidas

Bounce

Shake

Piscar

Excesso de movimento

---

# Dark Mode

Todos os componentes deverão possuir suporte nativo.

As cores nunca serão invertidas automaticamente.

Cada componente possuirá sua própria paleta.

---

# Acessibilidade

Contraste WCAG AA.

Navegação completa por teclado.

Labels obrigatórios.

ARIA Labels.

Focus visível.

---

# Internacionalização

Toda string deverá utilizar i18n.

Nenhum texto ficará hardcoded.

---

# Design Tokens

Exemplo

color-primary

color-success

color-danger

spacing-md

radius-lg

shadow-sm

font-size-body

---

# Filosofia

A interface deve desaparecer.

O usuário deve perceber apenas o aprendizado.

Todo componente existe para facilitar o estudo.

Nunca para chamar atenção para si mesmo.