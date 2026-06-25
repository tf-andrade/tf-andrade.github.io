# CLAUDE.md

Instruções para o Claude Code ao trabalhar neste repositório.

## O que é este projeto

Site pessoal de Tiago Andrade, hospedado no GitHub Pages em
https://tf-andrade.github.io/. É uma única página estática, **sem build, sem
dependências e sem framework**.

## Arquitetura

- Tudo vive em `index.html`: o HTML e o CSS (embutido em `<style>` no `<head>`).
  Não há arquivos JS, nem pasta de assets, nem package.json. O conteúdo já vem
  renderizado no HTML (nada é montado por JavaScript).
- Tema claro. O design usa variáveis CSS definidas em `:root`. Reaproveite essas
  variáveis (`--accent` é a cor de destaque terracota `#b1502f`; além de `--bg`,
  `--ink`, `--body`, `--muted`, `--line`, etc.) em vez de cores fixas.
- Tipografia em três famílias do Google Fonts, carregadas por um único `<link>`
  no `<head>`: **Newsreader** (serifada, para títulos/leads), **IBM Plex Sans**
  (corpo) e **IBM Plex Mono** (rótulos/eyebrows). Expostas como `--serif`,
  `--sans`, `--mono`. Esta é a única dependência externa do site.
- Layout: container `.wrap` central de `max-width: 1080px`. Cada seção usa
  `.section-grid` (grid de duas colunas: rótulo de 200px + conteúdo) separada
  por `border-top`.
- Responsivo: breakpoints em `@media (max-width: 720px)` (colunas viram uma só)
  e `@media (max-width: 480px)` (esconde os links do nav).

## Convenções

- Mantenha tudo em um único arquivo `index.html` a menos que o usuário peça
  explicitamente para separar CSS/JS.
- Ao adicionar conteúdo, siga o padrão das seções existentes (classes como
  `.exp-item`, `.row` para itens de writing/talks, `.contact-row`).
- Velocidade e peso são prioridade do usuário: mantenha o HTML enxuto (hoje
  ~16 KB) e **não introduza React, frameworks ou bundlers**. Evite novas
  dependências externas (CDNs etc.) sem alinhar antes.
- Texto da interface está em inglês; comentários e PR/commits podem ser em
  português (o usuário é brasileiro).

## Como publicar

O deploy é automático via GitHub Pages a partir da branch `main` (pasta raiz).
Para publicar uma mudança:

```bash
git add -A
git commit -m "Descrição da mudança"
git push
```

O Pages refaz o build em ~1 minuto. Não há etapa de build manual.

## Verificação

Para conferir uma alteração antes de publicar, basta abrir o `index.html` no
navegador localmente — não há servidor nem processo de build.
