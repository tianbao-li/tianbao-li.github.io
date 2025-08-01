{% for link in site.data.navigation.main %}
  {% if link.url contains 'http' %}
    <a class="{% if link.right %}right {% endif %}normal" 
       href="{{ link.url }}" 
       target="_blank" rel="noopener">
      {{ link.title }}
    </a>
  {% else %}
    <a class="{% if link.right %}right {% endif %}normal" 
       href="{{ link.url | relative_url }}">
      {{ link.title }}
    </a>
  {% endif %}
{% endfor %}