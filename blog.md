---
layout: page
title: Blog
permalink: /blog/
---

Textos sobre estudos, trabalho, leituras e outros interesses, do mais recente ao mais antigo.

<div class="blog-filters" role="group" aria-label="Filtrar artigos por categoria" style="margin: 1.25rem 0;">
  <label for="blog-category-filter">Categoria:</label>
  <select id="blog-category-filter" style="padding: .45rem .7rem; margin-left: .4rem; background: #222; color: #eee; border: 1px solid #777; border-radius: 5px;">
    <option value="all">Todas as categorias</option>
    <option value="life">Vida e reflexões</option>
    <option value="self-development">Desenvolvimento pessoal</option>
    <option value="technology">Tecnologia</option>
    <option value="research">Pesquisa</option>
    <option value="books">Livros</option>
    <option value="learning">Aprendizado</option>
    <option value="sports">Esportes</option>
  </select>
  <p id="blog-filter-status" role="status" aria-live="polite" style="font-size: .9em; margin-top: .5rem;"></p>
</div>

{% assign category_labels = "life:Vida e reflexões|self-development:Desenvolvimento pessoal|technology:Tecnologia|research:Pesquisa|books:Livros|learning:Aprendizado|sports:Esportes" | split: "|" %}
<ul class="post-list" id="blog-post-list">
  {% for post in site.posts %}
  <li data-category="{{ post.categories | first | escape }}">
    <time class="post-meta" datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: '%d/%m/%Y' }}</time>
    <h2><a class="post-link" href="{{ post.url | relative_url }}">{{ post.title | escape }}</a></h2>
    {% assign post_category = post.categories | first %}
    {% for item in category_labels %}
      {% assign parts = item | split: ":" %}
      {% if parts[0] == post_category %}<small>{{ parts[1] }}</small>{% endif %}
    {% endfor %}
  </li>
  {% endfor %}
</ul>

<script>
(function () {
  var filter = document.getElementById('blog-category-filter');
  var items = document.querySelectorAll('#blog-post-list > li');
  var status = document.getElementById('blog-filter-status');
  function update() {
    var selected = filter.value;
    var visible = 0;
    items.forEach(function (item) {
      var show = selected === 'all' || item.dataset.category === selected;
      item.hidden = !show;
      if (show) visible++;
    });
    status.textContent = visible + (visible === 1 ? ' artigo encontrado' : ' artigos encontrados');
  }
  filter.addEventListener('change', update);
  update();
})();
</script>

[Acompanhe por RSS]({{ '/feed.xml' | relative_url }}).
