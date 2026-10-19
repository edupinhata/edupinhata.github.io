# Continuidade

Atualizado em: 19/10/2026.

## Estado e autorização

Último envio: `9de95ef` em `origin/gh-pages`. Após duas revisões locais, o usuário aprovou explicitamente o novo layout com Blog e Microblog na entrada e organização automática das notas. Implementado, validado e aprovado pelo usuário na prévia; commit e push desta entrega autorizados em 19/10/2026. Demais mudanças de arquitetura continuam como propostas.

## Entrega

- `index.markdown`, `_layouts/landing.html`, `assets/home.css`: abertura compacta, Blog e Microblog em colunas distintas; no celular, blocos empilhados. Quatro posts recentes, três notas recentes e acervo ao final.
- `_config.yml`, `_microblog/*.md`, `_includes/microblog-list.html`, `Microblog.md`: coleção de 46 notas, ordenada por data; rascunhos e notas futuras ocultos. Histórico preservado em `/microblog/`, com âncora por nota. As datas de agosto seguem o dia/mês explícito, corrigindo o agrupamento antigo sob July/25.
- `blog.md`: arquivo completo dos posts em `/blog/`.
- `_ai/MICROBLOG.md`: instruções para adicionar notas sem duplicação; atualização automática acontece no build.
- `_ai/PLAN.md` e este arquivo: decisões e validações.
- Corrigido o link da entrada para a âncora real `formao-e-pesquisa` do About. About, posts e dependências do repositório preservados.

## Validações

- Build completo passou em Docker com Ruby 3.1, Jekyll 3.9.3 e Minima 2.5.1. Usada cópia temporária; plataforma adicionada apenas ao lockfile dessa cópia. Gemfile e lockfile originais intactos.
- Conferência das 46 datas e textos contra Microblog original passou.
- Teste de integração com nota temporária: inclusão automática, Markdown, exclusão de rascunho e data futura, IDs únicos e caminhos com baseurl `/preview` passou. Fixtures removidas da cópia temporária.
- Navegador: quatro posts e três notas na entrada, 46 notas no histórico, links locais e âncoras da entrada, acesso à nota e expansão de leituras passaram. Sem erros JS.
- Inspeção visual desktop (1440px) e celular (390px); testes de largura 320/390/768px sem overflow e ordem dos blocos correta. `git diff --check` passou.
- Restam avisos preexistentes de post_url em Cursos/Livros; não impediram o build. Sem auditoria dos links externos nem verificação de deploy.

## Ambiente e preservação

Docker iniciado para a validação. Prévia em `http://127.0.0.1:4000`, servida a partir de `/tmp/pinhata-preview-site`; fonte de build em `/tmp/pinhata-preview-source`, gems em `/tmp/pinhata-container-gems`. Esses diretórios são temporários.

Branch `gh-pages`. Preservados `.obsidian/`, `_posts/2026/` e os arquivos `output*.wav` não rastreados. A prévia inclui o post local de 2026, que continua não rastreado e não deve ser incluído inadvertidamente em commit. Reconsultar Git ao retomar.

## Próximo passo

Conferir a publicação após o envio autorizado. Consultar o histórico Git para o commit desta entrega. Não implementar as demais propostas por inferência.
