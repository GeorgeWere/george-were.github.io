<h2 style="margin-bottom:0; padding-top: 20px">[INDEX]</h2>

{% for index in site.index_menu %}
<div style="padding-top:10px">
  {% if page.url contains prj[1] %}
  > <strong style="color:orange">{{ index[0] }}</strong>
  {% else %}
  > <a href="{{ site.url }}/index/{{ index[1] }}.html">{{ index[0] }}</a>
  {% endif %}
</div>
{% endfor %}
