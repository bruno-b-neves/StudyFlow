# BaseButton

## Objetivo

O BaseButton representa o principal componente de ação do StudyFlow.

Ele é utilizado para iniciar ações, confirmar operações e navegar entre fluxos.

Não possui conhecimento de regras de negócio.

---

# Responsabilidade

Renderizar um botão consistente com o Design System.

---

# Não deve

Conhecer API.

Conhecer Vuex.

Conhecer Pinia.

Conhecer Backend.

Executar regras de negócio.

---

# Variants

Primary

Principal ação da tela.

Exemplo

Entrar

Salvar

Estudar

---

Secondary

Ações secundárias.

Exemplo

Cancelar

Voltar

Editar

---

Outlined

Ações alternativas.

---

Text

Ações discretas.

Exemplo

Esqueci minha senha

---

Danger

Operações destrutivas.

Excluir

Remover

---

# Sizes

Small

32px

---

Medium

40px

(Default)

---

Large

48px

---

# Width

Auto

Conteúdo

---

Full Width

100%

Muito utilizado no Mobile.

---

# States

Default

Hover

Focused

Pressed

Loading

Disabled

---

# Loading

Quando Loading

Desabilitar clique.

Mostrar Spinner.

Ocultar texto parcialmente.

---

# Icon

Pode possuir:

Ícone à esquerda.

Ícone à direita.

Somente ícone.

---

# Accessibility

Sempre possuir:

type

aria-label quando necessário

focus

keyboard navigation

---

# Props

variant

size

disabled

loading

fullWidth

startIcon

endIcon

type

---

# Slots

default

Texto do botão

---

# Emits

click

---

# Tokens utilizados

Colors

Spacing

Radius

Elevation

Typography

Motion

---

# Exemplos

Primary

[ Entrar ]

---

Secondary

[ Cancelar ]

---

Danger

[ Excluir ]

---

Icon

🔊 Ouvir

---

Loading

⟳ Salvando...

---

# Guidelines

Cada tela deve possuir apenas um botão Primary.

Evitar múltiplos botões Primary lado a lado.

A ação mais importante sempre deve utilizar o Variant Primary.