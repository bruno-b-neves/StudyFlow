# Study Session

## Objetivo

A Study Session é o núcleo do StudyFlow.

Seu objetivo é proporcionar uma experiência de estudo simples, rápida, imersiva e eficiente, baseada em repetição espaçada.

Durante uma sessão, o usuário responde Flashcards, avalia sua facilidade de lembrança e alimenta o algoritmo de aprendizagem.

---

# Público

Usuários autenticados.

---

# Objetivos de UX

- Eliminar distrações.
- Reduzir quantidade de cliques.
- Incentivar foco total.
- Tornar a revisão agradável.
- Minimizar esforço cognitivo.

---

# Objetivos de Negócio

- Aumentar sessões concluídas.
- Melhorar retenção.
- Aumentar tempo diário de estudo.
- Gerar dados para IA.

---

# Estrutura da Tela

A tela será composta por:

1. Header minimalista
2. Barra de progresso
3. Informações da sessão
4. Flashcard
5. Botões de resposta
6. Atalhos de teclado
7. Controles da sessão

---

# Header

Elementos

- Nome do Deck
- Botão Encerrar Sessão
- Configurações rápidas

Exemplo

🇺🇸 Inglês

[Configurações]

[X Encerrar]

---

# Barra de Progresso

Exibe

Flashcards concluídos

Flashcards restantes

Percentual

Exemplo

12 / 35

34%

████████░░░░░░░

---

# Informações da Sessão

Tempo da sessão

Flashcards restantes

Quantidade respondida

Exemplo

⏱ 08:25

📚 Restantes: 23

✅ Respondidos: 12

---

# Flashcard

Inicialmente será exibido apenas o Prompt.

Exemplo

House

---

# Mostrar Resposta

Botão

Mostrar resposta

Ao clicar

A Response será exibida.

Exemplo

House

↓

Casa

---

# Conteúdo do Flashcard

Prompt

Response

Pronúncia (opcional)

Exemplo

Observação

Imagem

Áudio

---

# Reprodução de Áudio

Caso exista áudio

Será exibido botão

▶ Ouvir

O usuário poderá reproduzir quantas vezes desejar.

No futuro

Reprodução automática configurável.

---

# Imagem

Caso exista

Será exibida abaixo da resposta.

---

# Exemplo

Caso exista

Será apresentado após a resposta.

Exemplo

This is my house.

---

# Observações

Caso existam

Serão exibidas abaixo do exemplo.

---

# Botões de Resposta

Após visualizar a resposta

Serão apresentados quatro botões.

Again

Hard

Good

Easy

---

# Again

Significado

Não consegui lembrar.

Consequências

Retorna para Learning.

Novo intervalo

30 segundos.

Incrementa Lapses.

---

# Hard

Significado

Lembrei com dificuldade.

Consequências

Pequeno aumento do intervalo.

Ease Factor reduzido levemente.

---

# Good

Significado

Resposta correta.

Consequências

Intervalo normal.

Mantém Ease Factor.

---

# Easy

Significado

Muito fácil.

Consequências

Grande aumento do intervalo.

Ease Factor aumenta.

---

# Atalhos

Espaço

Mostrar resposta

1

Again

2

Hard

3

Good

4

Easy

ESC

Encerrar sessão

---

# Configurações

Modo Escuro

Reprodução automática de áudio

Ocultar barra de progresso

Modo foco

Tela cheia

---

# Encerrar Sessão

Mensagem

Deseja realmente encerrar esta sessão?

Botões

Continuar estudando

Encerrar

---

# Sessão Concluída

Quando não existirem mais Flashcards.

Mensagem

Parabéns!

Você concluiu sua sessão de hoje.

Botão

Ver Resumo

---

# Estado Vazio

Mensagem

Nenhum Flashcard disponível.

Botão

Voltar ao Dashboard

---

# Estado de Carregamento

Skeleton apenas no primeiro Flashcard.

As próximas respostas devem ser instantâneas.

---

# Estado de Erro

Mensagem

Ocorreu um erro durante a sessão.

Botão

Tentar novamente.

---

# Componentes

StudyHeader

ProgressBar

StudyCard

AnswerButtons

AudioPlayer

ImageViewer

StatisticChip

ConfirmationDialog

---

# Navegação

Dashboard

↓

Deck

↓

Flashcards

↓

Study Session

↓

Study Summary

---

# Regras de Negócio

A sessão somente pode ser iniciada por usuário autenticado.

Somente Flashcards agendados para hoje serão apresentados.

Os Flashcards serão embaralhados dentro da sessão.

Cada resposta atualiza o CardProgress.

Again agenda nova revisão em aproximadamente 30 segundos.

Ao finalizar todos os Flashcards, a sessão é encerrada automaticamente.

---

# Performance

Pré-carregar os próximos Flashcards.

Pré-carregar imagens.

Pré-carregar áudios.

Resposta instantânea entre Flashcards.

---

# Responsividade

Desktop

Flashcard centralizado.

Tablet

Layout adaptado.

Mobile

Botões maiores.

Swipe futuramente.

---

# Acessibilidade

Todos os botões possuem labels.

Navegação por teclado.

Contraste WCAG AA.

Suporte a leitores de tela.

---

# Eventos

Study Session Started

Flashcard Revealed

Again Selected

Hard Selected

Good Selected

Easy Selected

Study Session Finished

---

# Métricas

Tempo médio da sessão.

Tempo por Flashcard.

Quantidade de respostas Again.

Quantidade de respostas Hard.

Quantidade de respostas Good.

Quantidade de respostas Easy.

Taxa de conclusão.

---

# Futuras Versões

Modo Full Screen.

Modo Pomodoro.

Modo Apenas Listening.

Modo Apenas Speaking.

Reconhecimento de voz.

Correção automática de pronúncia.

IA sugerindo revisões.

IA explicando erros.

Modo offline.

Sincronização em tempo real.

---

# Critérios de Aceitação

- O usuário pode iniciar uma sessão.
- Apenas Flashcards agendados são exibidos.
- A resposta permanece oculta até ação do usuário.
- Os botões Again, Hard, Good e Easy atualizam o progresso.
- A sessão termina automaticamente quando não houver mais Flashcards.
- O resumo é apresentado ao final da sessão.
- A tela funciona em Desktop, Tablet e Mobile.
- A navegação por teclado está disponível.