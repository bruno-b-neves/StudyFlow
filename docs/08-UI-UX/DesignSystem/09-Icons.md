# Icons

## Objetivo

O sistema de ícones do StudyFlow tem como objetivo facilitar a compreensão da interface, reduzir a carga cognitiva e tornar as ações mais intuitivas.

Os ícones complementam o texto.

Eles nunca devem substituir informações importantes.

---

# Biblioteca

Material Symbols Rounded

Motivos

- Inspirado no Material Design 3
- Excelente legibilidade
- Grande variedade de ícones
- Atualização constante
- Compatível com Web
- Compatível com Android
- Compatível com iOS

---

# Estilo

Rounded

Não utilizar:

- Sharp
- Filled
- Two Tone

Todo o sistema utilizará apenas uma família de ícones para manter consistência.

---

# Tamanho

Small

16px

Uso

Texto auxiliar

---

Medium

20px

Uso

Inputs

Buttons

---

Default

24px

Uso

Navbar

Cards

Menus

---

Large

32px

Uso

Empty States

Study Summary

---

Extra Large

48px

Uso

Dashboard

Ilustrações

---

# Peso

Utilizar sempre o peso padrão da biblioteca.

Evitar misturar diferentes pesos.

---

# Cor

A cor padrão segue o contexto do componente.

Exemplos

Botão Primário

Ícone branco

Botão Secundário

Ícone Primary

Erro

Ícone Error

Sucesso

Ícone Success

---

# Espaçamento

Ícone → Texto

8px

Ícone → Borda

16px

---

# Estados

Os ícones seguem exatamente os estados do componente.

Default

Hover

Focused

Disabled

Error

Success

---

# Acessibilidade

Todo ícone clicável deve possuir descrição.

Exemplo

aria-label="Criar novo deck"

Nunca utilizar apenas ícones para representar funcionalidades críticas.

Sempre acompanhar de texto quando necessário.

---

# Ícones principais do StudyFlow

Dashboard

home

---

Decks

folder

---

Flashcards

style

---

Estudar

school

---

Adicionar

add

---

Editar

edit

---

Excluir

delete

---

Pesquisar

search

---

Perfil

person

---

Configurações

settings

---

Logout

logout

---

Áudio

volume_up

---

Microfone

mic

---

Imagem

image

---

IA

auto_awesome

---

Estatísticas

analytics

---

Sequência

local_fire_department

---

Retenção

psychology

---

Tempo

schedule

---

Conquista

emoji_events

---

# Guidelines

Utilizar no máximo um ícone por ação.

Evitar excesso de ícones na mesma tela.

O conteúdo sempre deve ser o elemento principal.

Os ícones devem servir como apoio visual.

---

# Implementação

Todos os ícones serão encapsulados em um componente Vue.

Exemplo

<BaseIcon name="home" />

Nunca utilizar a biblioteca diretamente nas telas.

Isso facilita futuras substituições sem impacto na aplicação.