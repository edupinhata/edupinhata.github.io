---
layout: page
title: Revistas científicas
permalink: /revistas/
---
<link rel="stylesheet" href="{{ '/assets/revistas.css' | relative_url }}">

<div class="journals-page" lang="pt-BR" markdown="1">

Uma seleção de **20 revistas internacionais** para explorar pesquisas em otimização combinatória, grandes modelos de linguagem (LLMs) e a interface entre essas áreas.

**Referência: JIF 2025 · Consulta: 21/10/2026.** A lista está em ordem decrescente dos valores apresentados. É uma seleção temática, não uma lista exaustiva das maiores revistas nem um ranking absoluto de qualidade. Empates não indicam preferência.

<details markdown="1">
<summary>Como interpretar os indicadores e as fontes</summary>

O **Journal Impact Factor (JIF)** considera citações a publicações dos dois anos anteriores. O ano indicado é o da métrica, não o da consulta. Não é o JIF de cinco anos, CiteScore ou SJR. O indicador não mede a qualidade de um artigo individual nem substitui a avaliação do escopo da revista. [Definição e limites na Springer Nature](https://www.nature.com/natmachintell/journal-impact).

- **Fonte editorial:** valor e ano conferidos na página da revista ou editora.
- **Fonte secundária:** valor e ano conferidos em um agregador ou instituição, sem confirmação direta na editora ou no JCR.
- **Pendente:** informação da seleção inicial que não foi possível revalidar. Sua posição na lista é provisória.

Não houve consulta autenticada ao JCR. Algumas páginas editoriais bloquearam a leitura automática; resultados antigos de busca não foram usados para substituir valores de outro ano. As afinidades abaixo são uma avaliação temática para orientar leituras, não garantia de aceitação de trabalhos.

</details>

## Revistas por JIF

<ol class="journal-list">
{% for journal in site.data.revistas %}
  <li class="journal-card">
    <h3>{{ journal.name | escape }}</h3>
    <p class="journal-metric"><strong>JIF {{ journal.year }}: {{ journal.jif | replace: '.', ',' }}</strong>{% if journal.status == 'pendente' %} · valor provisório{% endif %}</p>
    <p>{{ journal.affinity | escape }}</p>
    <p class="journal-source">
      {% if journal.status == 'editorial' %}Fonte editorial{% elsif journal.status == 'secundária' %}Fonte secundária{% else %}Pendente de revalidação{% endif %}:
      <a href="{{ journal.source | escape }}">{{ journal.source_name | escape }}</a>.
      {% if journal.status == 'pendente' %}Valor 11,7 atribuído a 2025 na seleção inicial; não confirmado na página da revista nesta consulta. <a href="https://transacl.org/index.php/tacl">Página oficial da TACL</a>.{% endif %}
    </p>
  </li>
{% endfor %}
</ol>

## Caminhos de leitura

- **LLMs aplicados à otimização:** Computers &amp; Operations Research, EJOR, Expert Systems with Applications e Knowledge-Based Systems são pontos de partida temáticos.
- **Geração e avaliação de heurísticas:** Journal of Heuristics e IEEE Transactions on Evolutionary Computation.
- **Revisões de literatura:** ACM Computing Surveys e Artificial Intelligence Review.

Para escolher onde submeter um trabalho, confira também os artigos recentes e as diretrizes editoriais. Uma contribuição sobre LLMs precisa se adequar ao problema e ao tipo de evidência esperado em cada revista.

</div>
