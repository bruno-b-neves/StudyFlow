# ADR-001 - Estrutura do Flashcard

- **Status:** Aceito
- **Data:** 03/07/2026
- **Autor:** Bruno Neves

---

## Contexto

O StudyFlow é uma plataforma de aprendizagem baseada em repetição espaçada. O Flashcard representa a menor unidade de estudo dentro de um Deck e precisa ser suficientemente flexível para suportar diferentes tipos de conteúdo no futuro, como texto, áudio, imagem e outros recursos multimídia.

Durante a modelagem do domínio surgiu a necessidade de definir como um Flashcard deve representar seu conteúdo principal.

As opções consideradas foram:

- Front / Back
- Question / Answer
- Prompt / Response

---

## Problema

Como representar o conteúdo de um Flashcard de forma simples para a primeira versão da plataforma, mas que permita evolução sem necessidade de mudanças estruturais significativas?

---

## Opções consideradas

### Opção A — Front / Back

**Vantagens**

- Muito conhecida por usuários do Anki.
- Simples de compreender.

**Desvantagens**

- Terminologia fortemente associada ao conceito visual de um cartão.
- Pouco flexível para outros formatos de aprendizado.

---

### Opção B — Question / Answer

**Vantagens**

- Bastante intuitiva.
- Adequada para perguntas objetivas.

**Desvantagens**

- Nem todo Flashcard representa uma pergunta.
- Não se adapta bem a vocabulário, tradução ou associação de imagens.

---

### Opção C — Prompt / Response

**Vantagens**

- Terminologia mais genérica.
- Funciona para tradução, vocabulário, gramática, programação e qualquer outro domínio de estudo.
- Facilita futuras integrações com Inteligência Artificial.
- Permite expansão para múltiplos tipos de mídia.

**Desvantagens**

- Exige um pequeno período de adaptação para usuários acostumados com "Front" e "Back".

---

## Decisão

Foi adotada a estrutura **Prompt / Response** como representação oficial do conteúdo de um Flashcard.

Todo Flashcard deverá possuir obrigatoriamente:

- Prompt
- Response

Na primeira versão (MVP), ambos serão compostos obrigatoriamente por conteúdo textual.

---

## Consequências

### Positivas

- Arquitetura mais flexível.
- Independência do conceito visual de cartão.
- Facilidade para evolução futura.
- Melhor adaptação para diferentes áreas de conhecimento.
- Melhor integração com futuros recursos baseados em IA.

### Negativas

- Leve curva de aprendizado para usuários familiarizados com a nomenclatura tradicional utilizada pelo Anki.

---

## Decisões futuras relacionadas

Nas próximas versões será avaliada a inclusão de recursos multimídia associados ao Prompt e ao Response, como:

- Áudio
- Imagem
- Vídeo
- Arquivos complementares

Essa evolução deverá ocorrer sem necessidade de alterar a estrutura principal do Flashcard.

---

## Status da implementação

- [x] Decisão arquitetural aprovada.
- [ ] Modelagem do domínio.
- [ ] Modelagem do banco de dados.
- [ ] Implementação Backend.
- [ ] Implementação Frontend.