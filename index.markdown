---
layout: landing
title: Eduardo Pinhata
---
<div class="home-page">
  <header class="home-intro">
    <p class="home-eyebrow">Eduardo Pinhata · Pinhata Space</p>
    <h1>Ideias, estudos e prática</h1>
    <p>Aprendizados sobre software, liderança, otimização e IA — e outras leituras e reflexões pelo caminho.</p>
    <nav class="home-links" aria-label="Perfil">
      <a href="{{ '/about/' | relative_url }}">Sobre mim e contato</a>
      <a href="{{ '/about/#formao-e-pesquisa' | relative_url }}">Pesquisa em andamento</a>
    </nav>
  </header>

  <div class="home-columns">
    <section class="home-blog" aria-labelledby="blog-title">
      <header class="home-section-head">
        <h2 id="blog-title">Blog</h2>
        <p>Textos, estudos e leituras para desenvolver as ideias.</p>
      </header>
      {% for post in site.posts limit:4 %}
      <article class="home-post">
        <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: '%d/%m/%Y' }}</time>
        <h3><a href="{{ post.url | relative_url }}">{{ post.title | escape }}</a></h3>
        {% assign excerpt = post.description | default: post.excerpt | strip_html | normalize_whitespace %}
        {% assign excerpt_words = excerpt | split: ' ' | size %}
        {% if excerpt_words > 3 %}<p>{{ excerpt | truncatewords: 30 | escape }}</p>{% endif %}
      </article>
      {% else %}
      <p>As próximas publicações aparecerão aqui.</p>
      {% endfor %}
      <a class="home-section-link" href="{{ '/blog/' | relative_url }}">Todos os textos do blog →</a>
    </section>

    <section class="home-microblog" aria-labelledby="microblog-title">
      <header class="home-section-head">
        <h2 id="microblog-title">Microblog</h2>
        <p>Notas breves do cotidiano, do trabalho e dos estudos.</p>
      </header>
      {% include microblog-list.html limit=3 preview=true %}
      <a class="home-section-link" href="{{ '/microblog/' | relative_url }}">Todas as notas →</a>
    </section>
  </div>

  <section class="home-acervo" aria-labelledby="acervo-title">
    <h2 id="acervo-title">Explore o acervo</h2>
    <div class="home-acervo-links">
      <div>
        <h3><a href="{{ '/cursos/' | relative_url }}">Cursos</a></h3>
        <p>Registros de formação e notas de estudo.</p>
      </div>
      <div>
        <h3><a href="{{ '/livros/' | relative_url }}">Livros</a></h3>
        <p>Resumos e aprendizados de leituras.</p>
      </div>
      <div>
        <h3><a href="{{ '/feed.xml' | relative_url }}">Acompanhe por RSS</a></h3>
        <p>Receba os textos do blog no seu leitor.</p>
      </div>
    </div>
    <details>
      <summary>Leituras selecionadas</summary>
      <ul>
        {% capture selected_url %}{% post_url 2024/2024-09-05-sonarqube-sonarcloud-continuous-inspection-code-review-course %}{% endcapture %}
        <li><a href="{{ selected_url | relative_url }}">Qualidade de código com SonarQube e SonarCloud</a> — notas de um curso introdutório. Setembro de 2024, em inglês.</li>
        {% capture selected_url %}{% post_url 2024/2024-02-22-pratical-managing-skills-course %}{% endcapture %}
        <li><a href="{{ selected_url | relative_url }}">Practical Leadership Skills</a> — registro do curso, notas e certificado. Fevereiro de 2024, em inglês.</li>
        {% capture selected_url %}{% post_url 2024/2024-08-27-about-refactoring %}{% endcapture %}
        <li><a href="{{ selected_url | relative_url }}">Como demonstrar o valor da refatoração?</a> — rascunho com caminhos de estudo, ainda sem conclusões. Agosto de 2024, em inglês.</li>
      </ul>
    </details>
  </section>
</div>
