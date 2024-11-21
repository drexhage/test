## second

subdirectory

## Pages

{% assign pathCount = page.url | split:'/' | size | plus: 1 %}
{% for p in site.pages %}
{% assign ext = p.name | split:'.' | last %}
{% assign pCount = p.url | split:'/' | size %}
{% if ext == 'md' and p.url contains page.url and pCount == pathCount%}
- [{{p.title}}](/test{{p.url}})
{% endif %}
{% endfor %}

