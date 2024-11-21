## first

first 1!

{% capture url_path %}{{site.url}},,,{{page.url}}{% endcapture %}

{% assign pages = site.pages %}
{% for page in pages %}
{% assign ext = page.name | split:'.' | last %}
{% if ext == 'md' %}
- [{{page.title}}](/test{{page.url}}), {{page.name}}, {{page.url}}, {{page.ext}}, {{page.id}}, {{page.title}}, {{page.dir}}, {{page.path}}, {{page.slug}}, {{ext}}
{% endif %}
{% endfor %}

