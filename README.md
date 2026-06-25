# tf-andrade.github.io

Site pessoal de **Tiago Andrade**, publicado via [GitHub Pages](https://pages.github.com/).

🌐 **No ar em:** https://tf-andrade.github.io/

## Sobre

Página única (single-page), sem dependências e sem build. Todo o conteúdo,
estilo e estrutura ficam em um só arquivo: [`index.html`](index.html).
O CSS está embutido na própria página (`<style>` no `<head>`).

Seções: Hero · About · Experience · Articles & Talks · Contact.

## Como atualizar

O repositório é a fonte da verdade. Para alterar o site, edite o `index.html`
e publique:

```bash
git add -A
git commit -m "Atualiza o site"
git push
```

Em cerca de 1 minuto o GitHub Pages refaz o build e a mudança vai ao ar.

## Como funciona o GitHub Pages aqui

- O nome do repositório (`tf-andrade.github.io`) é especial: por isso o site
  vira a **página pessoal** na raiz do domínio, em vez de um subcaminho.
- O Pages serve a branch `main`, pasta raiz (`/`).
- HTTPS está habilitado.

## Estrutura

```
.
├── index.html   # o site inteiro (HTML + CSS)
├── README.md    # este arquivo
└── CLAUDE.md    # instruções para o Claude Code
```
