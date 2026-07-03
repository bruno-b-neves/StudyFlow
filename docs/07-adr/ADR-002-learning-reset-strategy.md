# ADR-002 - Estratégia de Reinício de Aprendizagem (Learning Reset Strategy)

- **Status:** Aceito
- **Data:** 03/07/2026
- **Autor:** Bruno Neves

---

## Contexto

O StudyFlow utiliza repetição espaçada para acompanhar a evolução do aprendizado dos usuários por meio da entidade `CardProgress`.

Durante a definição das regras de negócio surgiu a necessidade de estabelecer como a plataforma deve se comportar quando um usuário desejar reiniciar seus estudos em um Deck já estudado.

O principal desafio é equilibrar uma boa experiência do usuário com a preservação do histórico de aprendizagem para futuras análises e evoluções da plataforma.

---

## Problema

Quando um usuário optar por reiniciar seus estudos em um Deck, o que deve acontecer com os registros de progresso (`CardProgress`) existentes?

---

## Opções consideradas

### Opção A — Excluir o progresso

**Descrição**

Remover permanentemente todos os registros de `CardProgress` relacionados ao Deck.

**Vantagens**

- Implementação simples.
- Menor utilização de armazenamento.

**Desvantagens**

- Perda definitiva do histórico.
- Impossibilidade de auditoria.
- Estatísticas comprometidas.
- Futuras análises por IA tornam-se inviáveis.

---

### Opção B — Reiniciar o progresso existente

**Descrição**

Reutilizar o mesmo `CardProgress`, redefinindo seus valores para o estado inicial.

**Vantagens**

- Simples de implementar.
- Mantém apenas um registro por Flashcard.

**Desvantagens**

- Perde o histórico anterior.
- Não permite comparar diferentes ciclos de aprendizagem.
- Dificulta análises estatísticas.

---

### Opção C — Arquivar o progresso existente

**Descrição**

Arquivar os registros atuais de `CardProgress` e iniciar um novo ciclo de aprendizagem criando novos registros conforme os Flashcards forem novamente estudados.

**Vantagens**

- Preserva todo o histórico de aprendizagem.
- Permite auditoria.
- Possibilita comparação entre diferentes ciclos de estudo.
- Prepara o sistema para futuras funcionalidades baseadas em IA.
- Mantém estatísticas consistentes.

**Desvantagens**

- Maior complexidade de implementação.
- Crescimento gradual do volume de dados.

---

## Decisão

Foi adotada a **Opção C**.

Ao reiniciar o aprendizado de um Deck:

- O Deck permanece inalterado.
- Os Flashcards permanecem inalterados.
- Todos os `CardProgress` ativos relacionados ao Deck serão arquivados.
- Novos registros de `CardProgress` serão criados somente quando cada Flashcard for estudado novamente.

---

## Consequências

### Positivas

- Preservação completa do histórico de aprendizagem.
- Possibilidade de múltiplos ciclos de estudo.
- Base sólida para análises estatísticas.
- Preparação para recursos futuros de Inteligência Artificial.
- Maior flexibilidade para evolução do domínio.

### Negativas

- Necessidade de controlar registros ativos e arquivados.
- Crescimento do banco de dados ao longo do tempo.

---

## Decisões futuras relacionadas

No futuro poderão ser implementadas funcionalidades como:

- Visualização do histórico completo de ciclos de aprendizagem.
- Comparação entre ciclos de estudo.
- Restauração de um ciclo arquivado.
- Relatórios de evolução ao longo do tempo.
- Recomendações personalizadas baseadas em ciclos anteriores.

---

## Status da implementação

- [x] Decisão arquitetural aprovada.
- [ ] Modelagem do domínio.
- [ ] Modelagem do banco de dados.
- [ ] Implementação Backend.
- [ ] Implementação Frontend.