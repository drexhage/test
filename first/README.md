## first

first 1!

{% assign pages = site.pages %}
{% for page in pages %}
- [{{page.name}}]({{page.url}}), {{page.ext}}, {{page.id}}, {{page.title}}, {{page.dir}}, {{page.path}}, {{page.slug}}
{% endfor %}

