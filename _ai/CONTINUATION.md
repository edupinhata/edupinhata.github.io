# Continuidade

Atualizado em: 21/10/2026.

## Revistas científicas — 21/10/2026

- Pedido encaminhado pelo usuário: nova aba com 20 revistas relacionadas a otimização combinatória/LLMs, em ordem de JIF. Após revisar a prévia, usuário autorizou explicitamente commit e push desta página em 21/10/2026.
- Criados `revistas.md` (`/revistas/`), `_data/revistas.json` e `assets/revistas.css`; adicionada página ao `header_pages` em `_config.yml`. Lista em cartões para celular, ano, afinidades e fontes; metodologia expansível distingue JIF de outras métricas e seleção temática de ranking de qualidade.
- Conferência web: 9 métricas/anos confirmados em páginas editoriais (Nature, Springer e Computational Linguistics); 10 em fontes secundárias (Bioxbio e IIT Comillas); TACL 11,7/2025 mantido como provisório, explicitamente pendente. Não houve consulta autenticada ao JCR. Bloqueios de ACM/Elsevier/IEEE/MIT Press impedem confirmar todos os valores diretamente. Os 20 valores iniciais foram preservados com esses níveis de evidência.
- Verificação de dados: 20 nomes únicos, ordem decrescente, ano 2025 e links HTTPS passou. Build Jekyll/Minima em Docker passou (avisos preexistentes de post_url). Navegador confirmou 20 cartões, menu, detalhes expansíveis e ausência de overflow no desktop e a 390px. `git diff --check` passou; fontes externas consultadas conforme os níveis acima, sem garantia de acesso às páginas bloqueadas.
- Entrega preparada para commit e push autorizados em `gh-pages`; conferir histórico Git para o identificador e verificar deploy ao retomar. Arquivos locais alheios preservados.

## Tipografia aprovada — 21/10/2026

- Após comparar Source Sans 3, Georgia e Courier New, usuário escolheu Source Sans 3 e autorizou explicitamente commit e push.
- Entrega: `assets/main.scss`, `assets/fonts.css`, WOFF2 normal/itálica e licença Adobe em `assets/fonts/`, além de `mystyle.css` para as páginas históricas. Artigos mantêm 18px/1,65 da comparação; fonte monoespaçada de código preservada. Fontes hospedadas no site com `font-display: swap`.
- Comparador temporário removido, incluindo override de layout; posts voltam ao layout original do Minima. Demais conteúdos e arquivos locais preservados.
- Validação final: build Jekyll/Minima em Docker passou, mantendo avisos antigos de post_url. Navegador confirmou Source Sans 3 a 18px/29,7px, ausência do comparador e apresentação móvel sem overflow (354px efetivos). `git diff --check` passou.
- Commit principal `5d33517` enviado a `origin/gh-pages`. Ajuste posterior remove espaço final da licença original, sem mudar seu texto. Build e prévia validados; deploy remoto ainda não verificado. Prévia em `http://127.0.0.1:4000`.

## Diagnóstico de publicação — 20/10/2026

- Pedido: verificar ausência do post de Eleições 2026, sem autorização para commit, push ou publicação.
- HEAD local e último deploy: `2f15c6d`; post já rastreado e enviado. A observação abaixo sobre `_posts/2026/` não rastreado é histórica.
- O post declara `date: 2026-10-20 10:00 -0300`. O workflow `39373743949` iniciou às 02:13:31 de Brasília e terminou com sucesso às 02:14:10. A data futura explica a exclusão pelo Jekyll; `_config.yml` não habilita `future`.
- Consultadas API pública do GitHub, documentação do Jekyll e página inicial publicada: Silmarillion aparece, Eleições não. Às 08:52 de Brasília, o horário do post ainda não havia chegado. Não executado novo build local.
- Alterado somente este registro. Próximo passo: executar novo build após 10h ou, se o usuário autorizar publicação imediata, ajustar o horário do post e enviar a alteração. A passagem do horário sozinha não regenera o site estático.

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
