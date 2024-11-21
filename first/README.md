## first

first 1!

{{site.url}},,,{{page.url}}
{% assign pathCount = page.url | split:'/' | size | plus: 1 %}

{% for p in site.pages %}
{% assign ext = p.name | split:'.' | last %}
{% assign pCount = p.url | split:'/' | size %}
{% if ext == 'md' and p.url contains page.url and pCount == pathCount%}
- [{{p.title}}](/test{{p.url}}), {{p.name}}, {{p.url}}, {{p.ext}}, {{p.id}}, {{p.title}}, {{p.dir}}, {{p.path}}, {{p.slug}}, {{ext}}, {{pCount}}, {{pathCount}}, {{pCount + 1}}, {{pCount + 1 == pathCount}}
{% endif %}
{% endfor %}

