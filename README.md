# Diário de Aprendizados — Site de Estudos

Este repositório contém um site simples para organizar aulas, tutoriais e recursos sobre programação. O objetivo é ser um ponto de partida fácil de editar e expandir.

## Conteúdo principal

- `index.html` — página inicial com menu responsivo.
- `style.css` — estilos do site (inclui tema claro/escuro via `prefers-color-scheme`).
- `páginas/` — páginas de exemplo: `aulas.html`, `sobre.html`, `dotnet.html`.

## Como rodar localmente

Abra a pasta do projeto no terminal e execute um servidor HTTP simples (recomendado para que os links funcionem corretamente):

```bash
# com Python 3
python3 -m http.server 8000

# então abra no navegador:
http://localhost:8000
```

## Personalizar o menu e as cores

- Para alterar as cores e o tema, edite as variáveis CSS no início de `style.css` (seção `:root`). Exemplo:

  --bg: cor do fundo
  --fg: cor do texto
  --accent: cor dos links

- Para adicionar ou remover itens do menu, edite o `<ul id="primary-navigation">` dentro de `index.html`. Cada item é um `<li><a href="..."></a></li>`.

## Acessibilidade e testes rápidos

- O menu usa atributos `aria` (`aria-controls`, `aria-expanded`, `role="navigation"`) e pode ser aberto/fechado com o botão hamburger. Pressionar `Escape` fecha o menu.
- Verifique contraste, foco e navegação por teclado manualmente ou usando ferramentas como Lighthouse no DevTools.

## Adicionar novas páginas

Crie um novo arquivo HTML dentro da pasta `páginas/` e inclua um link para ele no menu (`index.html`). Exemplo mínimo:

```html
<!doctype html>
<html lang="pt-br">
  <head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <link rel="stylesheet" href="/style.css">
    <title>Nova Página</title>
  </head>
  <body>
    <header class="site-header">...</header>
    <main>Conteúdo</main>
  </body>
</html>
```

## Próximos passos sugeridos

- Implementar animação do hamburger para virar um X quando aberto.
- Marcar o item de menu ativo automaticamente (via JS ou server-side).
- Adicionar uma pequena trilha de aprendizado para a seção .NET (exercícios e projetos).

Se quiser, eu posso aplicar automaticamente a animação do hamburger e adicionar a trilha de .NET na página `páginas/dotnet.html`.

