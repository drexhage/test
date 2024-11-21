## first

first 1!

{% assign pages = site.pages %}
{% for page in pages %}
{% assign ext = page.path | split:'.' | last %}
{% if ext == 'md' %}
- [{{page.name}}](/test{{page.url}}), {{page.ext}}, {{page.id}}, {{page.title}}, {{page.dir}}, {{page.path}}, {{page.slug}}, {{ext}}
{% endif %}
{% endfor %}

