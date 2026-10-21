# Plano de organização do site

Atualizado em: 21/10/2026.
Estado: novo layout da entrada com Blog e Microblog autorizado e implementado; organização automática das notas incluída. Demais mudanças de arquitetura continuam como propostas.

## Objetivo e critérios

Decisão final de 21/10/2026: após comparar Source Sans 3, Georgia e Courier New, usuário aprovou Source Sans 3 e autorizou commit e push. Fonte hospedada localmente, artigos a 18px/1,65 e comparador removido. Demais propostas de arquitetura continuam pendentes.

Apresentar com clareza a atuação em engenharia e liderança e a formação e pesquisa em otimização e LLMs. Preservar o valor do arquivo pessoal, com contexto suficiente para IA e manutenção viável.

Critérios: percursos claros para mercado e academia; afirmações apoiadas em evidências; leitura rápida com aprofundamento opcional; contexto temporal explícito; poucas páginas e pouca duplicação.

## Diagnóstico de partida

- `about.markdown` já apresenta perfil, pesquisa em definição e contexto pessoal em detalhes expansíveis.
- `index.markdown` usa apenas `layout: home`; não possui apresentação ou curadoria própria.
- `_config.yml` mantém descrição de espaço pessoal e menu com About, Cursos, Livros, BlogsAndPeople e Microblog.
- Conteúdo técnico e acadêmico está disperso entre posts e microblog; faltam percursos temáticos próprios.
- Há textos em elaboração com seções vazias e materiais históricos sem uma hierarquia comum.
- A aparência renderizada e o build ainda não foram validados nesta análise.

## Sequência proposta

| Etapa | Proposta e entrega para revisão | Impacto | Esforço inicial / manutenção | Estado |
| --- | --- | --- | --- | --- |
| 1 | Entrada com apresentação breve, engenharia, pesquisa e conteúdos selecionados; descrição geral | Muito alto | Baixo / baixo | Implementada; novo layout validado em build e navegador |
| 2 | Desenhar mapa do site e destino dos índices existentes; inventariar correções de referências | Alto | Baixo a médio / baixo | Pendente |
| 3 | Selecionar evidências para Engenharia e liderança e Pesquisa; identificar lacunas sem inventar resultados | Alto | Médio / baixo | Pendente |
| 4 | Organizar Escritos por poucos temas, indicar estado editorial e distinguir arquivo histórico de contexto vigente | Alto | Médio / baixo | Pendente |
| 5 | Propor um ou dois relatos técnicos ou acadêmicos, com evidências necessárias e limites de divulgação | Alto | Médio a alto / ocasional | Pendente |
| 6 | Planejar extensão do padrão visual do About, convenção de idioma e validação de links, build e leitura móvel | Médio | Médio / baixo | Pendente |

O usuário autorizou implementar a Etapa 1 em 14/10/2026. Demais etapas continuam como propostas; correções nos índices existentes não fazem parte desta implementação.

## Arquitetura candidata — ainda não aceita

Menu: **Sobre · Engenharia e liderança · Pesquisa · Escritos**. Título do site leva ao início; contato nas páginas de perfil e rodapé.

- **Início (decisão atual):** abertura compacta, Blog e Microblog em colunas distintas no desktop e empilhados no celular; acervo e leituras selecionadas ao final.
- **Sobre:** perfil e formação, interesses pessoais resumidos, contato e contexto expansível para IA.
- **Engenharia e liderança:** frentes de atuação e seleção de problemas, decisões, aprendizados e evidências verificadas.
- **Pesquisa:** formação, orientação, estágio atual, problemas explorados, questões sobre LLMs e materiais acadêmicos verificados.
- **Escritos:** índices por engenharia e liderança; otimização e IA; leituras; reflexões pessoais.
- Cursos, livros e referências acessíveis por Escritos permanece proposta. Microblog passa a ter notas recentes na entrada e histórico em `/microblog/`; metas antigas continuam com organização pendente. Preservar URLs existentes.

Não criar de início uma página para cada interesse pessoal nem uma obrigação de publicação contínua.

## Verificações e candidatos de conteúdo

- `Livros.md`: referência de Código Limpo usa `2023-05-18`, mas o nome do arquivo usa `2023-05-15`; verificar resolução do `post_url` no build. Comunicação Não Violenta existe como post, mas não está no índice.
- `Cursos.md`: SonarQube está sob Leadership; avaliar agrupamento. O índice indica setembro e o post é de 05/09/2024: não há divergência de mês.
- `BlogsAndPeople.md`: está em `header_pages`, sem front matter; conferir resultado efetivo no menu antes de afirmar falha.
- Posts de refatoração e SonarQube: candidatos à seleção de engenharia, respeitando maturidade editorial.
- Microblog de julho de 2025: relatos de coloração de grafos e link de relatório; verificar contexto e evidências antes de transformá-los em relato acadêmico.
- `research_content/`: nome da pasta não prova vínculo com pesquisa acadêmica; revisar finalidade dos materiais.
- `goals/`: páginas históricas com layout próprio; considerar integração visual posteriormente.

## Decisões e perguntas abertas

Confirmado pelo usuário: preservar arquivos locais; valorizar atuação profissional e acadêmica; conteúdo pessoal complementar; leitura fácil; continuar iterando no plano; estrutura documental para IA, sem equipe de agentes.

Ainda aberto:

1. Nomes e quantidade de itens do menu.
2. Quanto conteúdo profissional deve ficar no Sobre e quanto nas páginas temáticas, evitando duplicação.
3. Quais textos destacar e quais manter apenas no arquivo.
4. Granularidade do contexto pessoal; presença do microblog na entrada foi aprovada.
5. Convenção de português e inglês.
6. Escopo de futuras implementações; o pedido atual cobre somente a Etapa 1.

Próximo passo: conferir publicação do novo layout; depois propor o mapa de navegação da Etapa 2. A arquitetura candidata não foi aprovada como definitiva.

## Implementação da Etapa 1

Entrada baseada no About, com percursos para suas seções profissionais e acadêmicas, três registros selecionados de 2024 (refatoração identificada como rascunho) e arquivo cronológico em posição secundária. Descrição geral em português. Menu, estilos e posts preservados. Verificações estáticas passaram; build bloqueado pela ausência do Bundler 2.4.12. Renderização e apresentação móvel pendentes.

## Revisão da entrada após feedback

O usuário considerou a primeira versão muito semelhante ao About e pediu melhoria. A revisão local substitui os resumos de atuação e formação por uma abertura curta, leituras comentadas e caminhos para o acervo. Perfil e pesquisa ficam acessíveis por links diretos ao About. A seleção conserva datas, idioma e identificação do rascunho. O usuário autorizou commit e push desta revisão em 19/10/2026; isso não implica aprovação das demais etapas ou da arquitetura candidata.

## Destaque do blog — 19/10/2026

Após a revisão, o usuário apontou que o blog ficou escondido no final. A entrada foi ajustada localmente para apresentar o Blog logo após a abertura, com cinco posts recentes e publicações anteriores em um bloco expansível. Leituras selecionadas e acervo vêm depois. Usado layout default com listagem Liquid explícita e classes do Minima, para controlar a ordem sem duplicar a lista automática do layout home. Essa revisão substitui a proposta de manter atualizações em posição secundária. Build e apresentação móvel ainda pendentes.

## Layout com Blog e Microblog — decisão de 19/10/2026

O usuário aprovou e autorizou implementar abertura compacta, Blog em coluna principal, Microblog lateral e acervo ao final; no celular, blocos empilhados. Também autorizou organizar as notas para alimentar automaticamente a entrada.

Implementação: layout `landing`, CSS próprio, quatro posts recentes, três notas recentes, arquivo do blog em `/blog/` e histórico em `/microblog/`. Coleção `_microblog/` com as 46 notas migradas; textos e datas conferidos. Instruções de manutenção em `MICROBLOG.md`. As notas futuras e os rascunhos ficam fora da listagem. Após revisar a prévia, o usuário aprovou o layout e autorizou commit e push em 19/10/2026.

Validação do novo layout: build Jekyll 3.9.3/Minima 2.5.1 em Docker; migração das 46 notas conferida; teste de nova nota, Markdown, rascunho, data futura e baseurl; links e âncoras da entrada; inspeção visual desktop e celular e larguras 320, 390 e 768px sem overflow. Permanecem avisos preexistentes de post_url em Cursos/Livros.
