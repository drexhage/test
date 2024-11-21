## first

first 1!

{{site.url}},,,{{page.url}}

{% assign pages = site.pages %}
{% for p in pages %}
{% assign ext = p.name | split:'.' | last %}
{% if ext == 'md' %}
{% if p.url contains {{page.url}} %}
- [{{p.title}}](/test{{p.url}}), {{p.name}}, {{p.url}}, {{p.ext}}, {{p.id}}, {{p.title}}, {{p.dir}}, {{p.path}}, {{p.slug}}, {{ext}}
{% endif %}
{% endif %}
{% endfor %}

