# Dashboard

## Objetivo

O Dashboard é a primeira tela exibida ao usuário após a autenticação.

Seu principal objetivo é responder rapidamente à pergunta:

> "O que devo estudar agora?"

A tela deve incentivar o estudo diário, apresentar o progresso do usuário e oferecer acesso rápido às funcionalidades mais importantes da plataforma.

---

# Público

Usuários autenticados.

---

# Objetivos de UX

- Reduzir a fricção para iniciar uma sessão de estudos.
- Mostrar claramente o progresso do usuário.
- Incentivar consistência através de métricas visuais.
- Facilitar a navegação para os Decks.
- Motivar o usuário a retornar diariamente.

---

# Objetivos de Negócio

- Aumentar retenção diária.
- Aumentar tempo médio de estudo.
- Incentivar criação de novos Decks.
- Melhorar taxa de conclusão das sessões.
- Preparar o usuário para futuras funcionalidades de IA.

---

# Estrutura da Página

A tela será composta pelas seguintes seções.

1. Header
2. Saudação
3. Resumo diário
4. Botão principal de estudo
5. Estatísticas
6. Lista de Decks
7. Ações rápidas
8. Recomendação da IA (V2)

---

# Header

Componentes

- Logo StudyFlow
- Avatar do usuário
- Menu
- Notificações (V2)

---

# Saudação

Exemplos

Bom dia, Bruno 👋

Boa tarde 👋

Boa noite 👋

A saudação será definida conforme o horário local do usuário.

---

# Resumo Diário

Apresenta rapidamente o estado atual do aprendizado.

Campos

🔥 Sequência de estudos

📚 Flashcards disponíveis hoje

⏱ Tempo médio

🎯 Retenção

📈 Nível

Exemplo

🔥 12 dias consecutivos

📚 35 Flashcards para hoje

⏱ Média: 18 minutos

🎯 Retenção: 91%

📈 Intermediário

---

# Botão Principal

O principal Call To Action da tela.

Texto

Iniciar Sessão

Ação

Inicia imediatamente uma nova sessão de estudos.

Caso não existam Flashcards disponíveis:

O botão será desabilitado.

Mensagem

"Você não possui Flashcards disponíveis para estudar."

Será apresentado um botão:

Criar novo Deck

---

# Estatísticas

Cards pequenos contendo indicadores rápidos.

Campos

Tempo estudado hoje

Flashcards estudados hoje

Flashcards revisados

Sequência atual

Maior sequência

Retenção média

Tempo médio por sessão

Sessões concluídas

Exemplo

Hoje

25 Flashcards

18 minutos

Retenção

91%

---

# Lista de Decks

Lista todos os Decks cadastrados.

Cada Card deve conter

Nome

Idioma

Descrição

Quantidade de Flashcards

Flashcards pendentes

Último estudo

Status

Exemplo

🇺🇸 Inglês

320 Flashcards

23 para hoje

Último estudo

Hoje às 08:15

Status

Ativo

---

# Ações do Deck

Cada Deck permitirá

Abrir

Editar

Arquivar

Excluir

Exportar (V2)

Compartilhar (V2)

---

# Estado Vazio

Caso não existam Decks.

Mensagem

Você ainda não possui nenhum Deck.

Botão

Criar meu primeiro Deck

Ilustração amigável.

---

# Estado de Carregamento

Utilizar Skeleton Loading.

Nunca utilizar Spinner central.

Elementos

Resumo

Cards

Decks

Estatísticas

Todos utilizando Skeleton.

---

# Estado de Erro

Mensagem

Não foi possível carregar seu Dashboard.

Botão

Tentar novamente

---

# Recomendações Inteligentes (V2)

Esta seção será alimentada pela IA.

Exemplos

Você possui dificuldade com verbos irregulares.

Hoje seria interessante revisar o Present Perfect.

Seu desempenho caiu nos últimos três dias.

Deseja fazer uma sessão rápida de revisão?

---

# Componentes Utilizados

Header

Avatar

PrimaryButton

StatisticCard

StudySummaryCard

DeckCard

EmptyState

SkeletonCard

ErrorState

Badge

ProgressBar

Dropdown

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

↓

Dashboard

---

# Regras de Negócio

O Dashboard somente poderá ser acessado por usuários autenticados.

As estatísticas sempre considerarão o fuso horário do usuário.

A quantidade de Flashcards para hoje será calculada pelo algoritmo de repetição espaçada.

A retenção será baseada nas respostas registradas pelo usuário.

O nível será determinado futuramente pela IA.

---

# Permissões

Usuário autenticado

Pode visualizar apenas seus próprios Decks.

Pode iniciar sessões.

Pode editar seus próprios Decks.

Não pode visualizar dados de outros usuários.

---

# Performance

Tempo máximo de carregamento

2 segundos.

As informações serão carregadas de forma assíncrona.

Caso uma seção falhe, as demais continuarão sendo exibidas.

---

# Responsividade

## Desktop

Layout em Grid.

Resumo na parte superior.

Estatísticas em Cards.

Decks abaixo.

## Tablet

Cards em duas colunas.

Lista de Decks abaixo.

## Mobile

Layout vertical.

Botão de iniciar sessão sempre visível.

Cards empilhados.

---

# Acessibilidade

Todos os botões possuirão labels.

Ícones terão descrição para leitores de tela.

Contraste mínimo WCAG AA.

Navegação completa via teclado.

---

# Eventos

Dashboard Opened

Study Session Started

Deck Selected

Create Deck Clicked

Retry Dashboard Clicked

---

# Métricas

Tempo médio até iniciar sessão.

Quantidade de acessos diários.

Taxa de retorno.

Quantidade de Decks criados.

Sessões iniciadas.

Sessões concluídas.

---

# Futuras Versões

Integração com IA.

Calendário de estudos.

Ranking pessoal.

Objetivos semanais.

Conquistas.

Gráficos de evolução.

Sugestões automáticas.

Recomendações inteligentes.

---

# Critérios de Aceitação

- O Dashboard deve carregar corretamente após o login.
- O usuário deve visualizar apenas seus próprios dados.
- O botão "Iniciar Sessão" deve iniciar imediatamente uma sessão.
- O Dashboard deve funcionar em Desktop, Tablet e Mobile.
- O estado vazio deve orientar a criação do primeiro Deck.
- Os Skeletons devem substituir Spinners.
- O Dashboard deve permanecer utilizável caso uma seção falhe.