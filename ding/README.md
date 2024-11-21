## Ding

ding halt

## Pages

{% assign pathCount = page.url | split:'/' | size %}
{% for p in site.pages %}
{% assign ext = p.name | split:'.' | last %}
{% assign pCount = p.url | split:'/' | size %}
{% if ext == 'md' and p.url contains page.url and pCount + 1 == pathCount%}
- [{{p.title}}](/test{{p.url}})
{% endif %}
{% endfor %}
