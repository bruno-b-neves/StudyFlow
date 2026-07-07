# Study Summary

## Objetivo

A tela de Study Summary apresenta os resultados da sessão recém-concluída.

Seu objetivo é:

- Reforçar a sensação de progresso.
- Motivar continuidade dos estudos.
- Exibir métricas relevantes.
- Incentivar a próxima sessão.
- Aumentar retenção diária.

---

# Público

Usuários autenticados.

---

# Objetivos de UX

- Gerar sensação de conquista.
- Reforçar hábitos de estudo.
- Tornar o progresso visível.
- Evitar excesso de informações.

---

# Objetivos de Negócio

- Aumentar frequência de estudos.
- Melhorar retenção.
- Aumentar taxa de retorno diário.
- Incentivar sessões futuras.

---

# Estrutura da Tela

A tela será composta por:

1. Mensagem de conclusão
2. Resumo da sessão
3. Estatísticas
4. Evolução
5. Próximos estudos
6. Ações rápidas

---

# Mensagem Principal

Exemplo

🎉 Parabéns!

Você concluiu sua sessão de estudos.

ou

🔥 Excelente trabalho!

Você manteve sua sequência de estudos.

---

# Resumo da Sessão

Exibir:

Quantidade estudada

Tempo total

Retenção

Desempenho

Exemplo

📚 35 Flashcards revisados

⏱ 18 minutos

🎯 Retenção: 91%

📈 Desempenho: Muito bom

---

# Estatísticas da Sessão

Mostrar

Again

Hard

Good

Easy

Exemplo

Again

4

Hard

6

Good

18

Easy

7

---

# Gráfico de Distribuição

Representação visual simples.

Exemplo

Again

■■

Hard

■■■

Good

■■■■■■■■

Easy

■■■■

---

# Sequência de Estudos

Exibir

Sequência atual

Maior sequência

Exemplo

🔥 Sequência atual

12 dias

🏆 Maior sequência

24 dias

---

# Evolução

Comparação com sessões anteriores.

Exemplo

Hoje

35 Flashcards

Ontem

28 Flashcards

Variação

+25%

---

# Próximas Revisões

Exibir

Quantidade prevista para amanhã.

Exemplo

📅 Amanhã você terá

42 Flashcards para revisar.

---

# Nível do Usuário

Exibir nível atual.

Exemplo

📈 Intermediário

---

# Conquistas (V2)

Exemplos

Primeira sessão

7 dias consecutivos

30 dias consecutivos

100 Flashcards estudados

1000 Flashcards estudados

---

# Recomendação da IA (V2)

Exemplo

💡 Você apresentou dificuldade em verbos irregulares.

Deseja revisar esse conteúdo amanhã?

---

# Ações Disponíveis

Botão

Voltar ao Dashboard

Botão

Continuar Estudando

Botão

Abrir Deck

---

# Estado de Carregamento

Skeleton Loading.

Nunca Spinner central.

---

# Estado de Erro

Mensagem

Não foi possível carregar o resumo.

Botão

Voltar ao Dashboard

---

# Componentes

SummaryCard

StatisticCard

ProgressCard

StreakCard

PrimaryButton

SecondaryButton

AchievementCard

ChartCard

---

# Navegação

Study Session

↓

Study Summary

↓

Dashboard

---

# Regras de Negócio

Somente sessões concluídas geram resumo.

As estatísticas refletem apenas a sessão atual.

A sequência será atualizada apenas após conclusão da sessão.

A retenção será recalculada ao final.

---

# Performance

Carregamento inferior a 1 segundo.

Dados já disponíveis ao finalizar sessão.

---

# Responsividade

Desktop

Cards lado a lado.

Tablet

Grid reduzido.

Mobile

Cards empilhados.

Botões em largura total.

---

# Acessibilidade

Contraste WCAG AA.

Navegação por teclado.

Leitores de tela.

Labels acessíveis.

---

# Eventos

Study Summary Opened

Continue Studying Clicked

Dashboard Clicked

Deck Opened

---

# Métricas

Sessões concluídas.

Tempo médio.

Retenção.

Sequência.

Taxa de retorno.

---

# Futuras Versões

Gráficos avançados.

Calendário de estudos.

Conquistas.

IA personalizada.

Relatórios semanais.

Relatórios mensais.

Gamificação.

Ranking pessoal.

---

# Critérios de Aceitação

- O resumo é exibido ao final da sessão.
- Todas as estatísticas são apresentadas corretamente.
- A sequência é atualizada.
- O usuário pode retornar ao Dashboard.
- O usuário pode iniciar nova sessão.
- Layout responsivo.
- Skeleton Loading implementado.