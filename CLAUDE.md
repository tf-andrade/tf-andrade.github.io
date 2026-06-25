# CLAUDE.md

Instruções para o Claude Code ao trabalhar neste repositório.

## O que é este projeto

Site pessoal de Tiago Andrade, hospedado no GitHub Pages em
https://tf-andrade.github.io/. É uma única página estática, **sem build, sem
dependências e sem framework**.

## Arquitetura

- Tudo vive em `index.html`: o HTML e o CSS (embutido em `<style>` no `<head>`).
  Não há arquivos JS, nem pasta de assets, nem package.json.
- O design usa variáveis CSS definidas em `:root` (cores, fonte). Reaproveite
  essas variáveis (`--bg`, `--surface`, `--border`, `--text`, `--muted`,
  `--accent`, etc.) em vez de cores fixas (hardcoded).
- Layout: container central de `max-width: 720px`. Seções separadas por
  `border-bottom`. Tema escuro.
- Há um breakpoint responsivo em `@media (max-width: 600px)`.

## Convenções

- Mantenha tudo em um único arquivo `index.html` a menos que o usuário peça
  explicitamente para separar CSS/JS.
- Ao adicionar conteúdo, siga o padrão das seções existentes (classes como
  `.exp-item`, `.article-item`, `.contact-link`).
- Texto da interface está em inglês; comentários e PR/commits podem ser em
  português (o usuário é brasileiro).
- Não introduza dependências externas (CDNs, frameworks) sem alinhar antes.

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
