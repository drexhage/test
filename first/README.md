## first

first 1!

{{site.url}},,,{{page.url}}
{% assign pathCount = page.url | split:'/' | count %}

{% assign pages = site.pages %}
{% for p in pages %}
{% assign ext = p.name | split:'.' | last %}
{% assign pCount = p.url | split:'/' | count %}
{% if ext == 'md' and p.url contains page.url and pathCount == pCount %}
- [{{p.title}}](/test{{p.url}}), {{p.name}}, {{p.url}}, {{p.ext}}, {{p.id}}, {{p.title}}, {{p.dir}}, {{p.path}}, {{p.slug}}, {{ext}}
{% endif %}
{% endfor %}

