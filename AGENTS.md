---
published: false
---

# Orientações para IA

## Retomada

1. Leia `_ai/CONTINUATION.md` para conhecer o estado e o escopo autorizado.
2. Leia `_ai/PLAN.md` para consultar a sequência proposta e as decisões pendentes.
3. Confira `git status --short --branch` e as instruções aplicáveis antes de editar.
4. Para decisões editoriais, leia `about.markdown`, `assets/about.css` e os arquivos envolvidos. O estado atual dos arquivos prevalece sobre observações antigas.

## Objetivo editorial

- Valorizar engenharia de software, liderança e formação e pesquisa acadêmica em otimização combinatória e LLMs.
- Usar conteúdo pessoal como complemento e contexto útil para assistentes, sem transformar o site em inventário da rotina.
- Favorecer leitura rápida, listas, destaques, tabelas úteis e detalhes expansíveis.
- Considerar visitantes do mercado de trabalho, comunidade acadêmica e assistentes de IA.
- Preferir soluções simples de manter, compatíveis com o tempo disponível do autor.

## Evidências e conteúdo

- Use o About como referência de perfil; não replique toda a biografia nos documentos de trabalho.
- Distinga fatos declarados, interpretações, propostas e decisões aceitas.
- Não invente traços de personalidade, experiências, resultados, métricas ou publicações.
- Distinga pesquisa em exploração, tema definido, trabalho de disciplina e publicação.
- Preserve datas e indique caráter histórico. Confirme a vigência de metas datadas antes de usá-las como prioridades atuais.
- Responda em português, salvo orientação diferente do usuário.

## Escopo e preservação

- O plano é uma proposta revisável, não autorização para executá-lo.
- Na fase atual, edite apenas esta documentação de trabalho quando solicitado; não altere conteúdo, estilos ou configuração do site.
- Preserve alterações e arquivos locais, inclusive não rastreados. Não use reset, clean ou descarte de conteúdo para preparar o trabalho.
- Não faça commit, push ou publicação sem autorização do usuário. Uma autorização posterior pode ampliar o escopo; registre-a na continuidade.
- Não crie estrutura de múltiplos agentes por causa do nome deste arquivo.

## Continuidade e verificação

- Ao encerrar trabalho relevante, atualize `_ai/CONTINUATION.md` com resultado, arquivos alterados, validações, limitações e próximo passo.
- Atualize `_ai/PLAN.md` quando houver mudança de proposta ou decisão explícita. Não marque uma proposta como aceita por silêncio.
- Mantenha os registros curtos e úteis para retomada, sem transcrever conversas ou dados pessoais desnecessários.
- Para futuras mudanças no site, valide links e geração; para mudanças visuais, confira também a apresentação em telas pequenas. Não declare verificações que não executou.

## Organização

- Site Jekyll com tema Minima; configuração em `_config.yml`, posts em `_posts/`.
- Documentos de trabalho ficam em `_ai/`, fora da organização pública de páginas. Não adicione front matter de página nem links públicos para esses documentos.
- Este arquivo tem `published: false` para não se tornar uma página pública em Jekyll.
