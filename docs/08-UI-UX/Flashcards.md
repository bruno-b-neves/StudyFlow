# Flashcards

## Objetivo

A tela de Flashcards permite ao usuário criar, visualizar, editar e organizar os cartões de estudo pertencentes a um Deck.

Cada Flashcard representa a menor unidade de aprendizado dentro do StudyFlow.

Um Flashcard é composto obrigatoriamente por um Prompt e uma Response.

Exemplos

Prompt

House

Response

Casa

ou

Prompt

How are you?

Response

Como você está?

---

# Público

Usuários autenticados.

---

# Objetivos de UX

- Tornar a criação de Flashcards extremamente rápida.
- Facilitar revisões.
- Reduzir quantidade de cliques.
- Organizar grandes quantidades de Flashcards.
- Incentivar estudo contínuo.

---

# Objetivos de Negócio

- Aumentar quantidade de Flashcards criados.
- Melhorar retenção.
- Facilitar aprendizado.
- Preparar integração com IA.

---

# Estrutura da Página

A tela será composta por

1. Header
2. Informações do Deck
3. Barra de Pesquisa
4. Lista de Flashcards
5. Botão Criar Flashcard
6. Paginação (caso necessário)

---

# Header

Componentes

Breadcrumb

Título

Botão Novo Flashcard

Exemplo

Dashboard

>

Inglês

>

Flashcards

---

# Informações do Deck

Nome

Idioma

Quantidade de Flashcards

Última atualização

Exemplo

🇺🇸 Inglês

320 Flashcards

Atualizado hoje

---

# Barra de Pesquisa

Placeholder

Pesquisar Flashcard...

Pesquisa em

Prompt

Response

Tags (V2)

---

# Lista de Flashcards

Cada Flashcard será apresentado em Card.

Cada Card deverá mostrar

Prompt

Response

Data de criação

Última edição

Status

---

# Exemplo

Prompt

Apple

↓

Response

Maçã

Criado

15/06/2026

Status

Ativo

---

# Estrutura do Flashcard

Campos obrigatórios

Prompt

Response

Campos opcionais

Observação

Pronúncia

Áudio

Imagem

Exemplo de uso

Tags (V2)

Nível de dificuldade (V2)

---

# Áudio

O usuário poderá anexar

MP3

WAV

OGG

Objetivo

Treinar Listening.

---

# Imagem

Opcional.

Objetivo

Facilitar memorização.

---

# Criar Flashcard

Botão

Novo Flashcard

Campos

Prompt

Response

Observação

Pronúncia

Áudio

Imagem

Botões

Cancelar

Salvar

---

# Editar Flashcard

Pode alterar

Prompt

Response

Observação

Pronúncia

Imagem

Áudio

---

# Excluir Flashcard

Mensagem

Deseja realmente excluir este Flashcard?

Botões

Cancelar

Excluir

---

# Estado Vazio

Mensagem

Este Deck ainda não possui Flashcards.

Botão

Criar primeiro Flashcard.

---

# Estado de Carregamento

Skeleton para

Lista

Cards

Pesquisa

---

# Estado de Erro

Mensagem

Não foi possível carregar os Flashcards.

Botão

Tentar novamente.

---

# Componentes Utilizados

Header

FlashcardCard

SearchInput

PrimaryButton

Modal

EmptyState

SkeletonCard

ConfirmationDialog

AudioPlayer

ImagePreview

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

Prompt é obrigatório.

Response é obrigatória.

Prompt e Response não podem estar vazios.

Áudio é opcional.

Imagem é opcional.

Observação é opcional.

Todo Flashcard pertence a um único Deck.

Ao ser criado, o Flashcard ainda não possui progresso de estudo.

O progresso será criado automaticamente após a primeira revisão.

---

# Permissões

Usuário autenticado

Pode criar Flashcards.

Pode editar apenas Flashcards próprios.

Pode excluir apenas Flashcards próprios.

---

# Performance

Pesquisa instantânea.

Paginação.

Lazy Loading.

Upload assíncrono de imagens.

Upload assíncrono de áudio.

---

# Responsividade

## Desktop

Lista em Cards.

## Tablet

Cards reduzidos.

## Mobile

Cards empilhados.

Botão Novo Flashcard fixo.

---

# Acessibilidade

Leitores de tela.

Contraste WCAG AA.

Labels em todos os campos.

Navegação por teclado.

---

# Eventos

Flashcard Created

Flashcard Updated

Flashcard Deleted

Flashcard Viewed

Audio Played

Image Opened

---

# Métricas

Quantidade de Flashcards.

Flashcards criados por dia.

Tempo médio de criação.

Quantidade média por Deck.

Flashcards estudados.

---

# Futuras Versões

Geração automática por IA.

Importação por PDF.

Importação por DOCX.

Importação por legendas.

OCR.

Reconhecimento de imagens.

Tradução automática.

Correção automática.

Geração de exemplos.

Pronúncia via IA.

---

# Critérios de Aceitação

- O usuário pode criar Flashcards.
- Prompt é obrigatório.
- Response é obrigatória.
- O Flashcard pertence obrigatoriamente a um Deck.
- Áudio é opcional.
- Imagem é opcional.
- Pesquisa funciona corretamente.
- Estado vazio implementado.
- Skeleton implementado.
- Layout responsivo.