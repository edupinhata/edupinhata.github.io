# Como publicar no microblog

As notas ficam em `_microblog/`, uma nota por arquivo Markdown. A página inicial mostra as três mais recentes; `/microblog/` reúne todas. Ambas usam a mesma coleção e o include `_includes/microblog-list.html`.

## Nova nota

Crie `_microblog/AAAA-MM-DD-assunto.md`, com data explícita e fuso:

```markdown
---
date: 2026-10-19 12:00:00 -0300
---

Texto da nota. Pode usar **ênfase**, links e parágrafos em Markdown.
```

Use um nome diferente para cada nota, inclusive quando houver mais de uma no mesmo dia; a hora define a ordenação dentro do dia. O nome do arquivo forma a âncora da nota no histórico, por isso evite renomeá-lo depois de publicar.

- Para rascunhos, acrescente `published: false` ao front matter.
- Notas com data futura não aparecem antes dessa data. Elas entram na próxima geração do site após a data; Jekyll não agenda sozinho uma nova publicação.
- A atualização da página inicial e do histórico acontece no build, depois do fluxo habitual de commit, push e publicação.
- Edite o arquivo original da nota para corrigir seu conteúdo. Não copie o texto para `index.markdown` ou `Microblog.md`.
- As notas não entram na lista nem no RSS do blog, que continuam usando `_posts/`.

## Migração

As 46 notas existentes foram extraídas de `Microblog.md`, preservando textos e datas. As entradas de 30 e 31/08/2025 usam o mês explícito no registro; o título de mês antigo dizia July/25. A URL `/microblog/` foi preservada e cada nota passou a ter uma âncora própria.
