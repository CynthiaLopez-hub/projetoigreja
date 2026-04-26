# Tela de Login - Assembleia de Deus

Este repositório contém uma página de login em HTML com estilo CSS embutido. A página é composta por duas colunas: um lado esquerdo com informações e imagem, e um lado direito com o formulário de login.

## Estrutura do código

### HTML

- `<!DOCTYPE html>`: define o documento como HTML5.
- `<html lang="PT-BR">`: define o idioma como português do Brasil.
- `<head>`:
  - `<meta charset="UTF-8">`: define a codificação de caracteres para UTF-8.
  - `<title>`: título da página de login.
  - `<link>` para a fonte `Poppins` do Google Fonts.
  - `<link>` para os ícones do Bootstrap Icons.
  - `<style>`: contém todo o CSS usado na página.

### Corpo (`<body>`)

A página principal usa uma `div` com a classe `.tela-login`.

- `.lado-esquerdo`: área de apresentação com fundo escuro, texto branco, imagem e mensagem.
- `.lado-direito`: área do formulário de login.
- O formulário contém campos de e-mail, senha, opção "Lembrar-me" e botão de entrar.

## CSS principal

O CSS dentro da tag `<style>` define o comportamento e o visual da página.

### Regras básicas

- `.tela-login` é um container flexível (`display: flex`) que ocupa toda a altura da tela (`height: 100vh`).
- `.lado-esquerdo` e `.lado-direito` usam `flex: 1` para dividir igualmente o espaço.
- `.lado-esquerdo` tem cor de fundo `#0a1f3d`, texto branco e conteúdo centralizado.
- A imagem dentro de `.lado-esquerdo` recebe largura de `300px`, cantos arredondados e opacidade `0.8`.
- `.lado-direito` centraliza o formulário dentro da área disponível.
- Inputs e botão recebem estilo para preencher a largura, ter espaçamento e bordas arredondadas.

## O que faz `@media`?

A seção `@media (max-width: 768px)` é usada para tornar a página responsiva em telas menores, como tablets e celulares.

### Como funciona

- `@media (max-width: 768px)` significa: "aplicar os estilos abaixo apenas quando a largura da janela for igual ou menor que 768 pixels".
- Isso cria uma regra de CSS chamada *media query*.
- Quando o dispositivo é pequeno, os estilos dentro dessa regra substituem os estilos padrão.

### O que muda no código

Dentro de `@media` existem duas regras:

- `.tela-login { flex-direction: column; }`
  - Em vez de posicionar os dois lados lado a lado, o layout passa a ser empilhado verticalmente.
  - Isso é mais adequado para telas estreitas, onde duas colunas lado a lado podem ficar apertadas.

- `.lado-esquerdo { display: none; }`
  - A coluna esquerda é escondida completamente em telas pequenas.
  - Assim, o foco é mantido no formulário de login sem ocupar espaço com a imagem e o texto extra.

### Por que isso é útil?

- Melhora a experiência em dispositivos móveis.
- Evita que a página fique cortada ou difícil de usar em telas pequenas.
- Faz com que o formulário de login apareça sozinho, de forma mais limpa e direta.

## Observações

O código atual tem alguns pontos que podem ser ajustados para funcionar melhor:

- A regra `* { box-sizing: border-box; font-family: 'Poppins', sans-serif; }` está dentro do seletor `body { ... }`. O ideal é colocá-la fora, no topo do CSS.
- A classe `.container.form>` na estrutura HTML está escrita de forma incorreta. O correto seria algo como `<div class="container-form">`.

Esses ajustes não mudam o propósito do código, mas ajudam a garantir que ele funcione corretamente em todos os navegadores.
