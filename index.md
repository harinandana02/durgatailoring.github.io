---
layout: substitute

title: Photo Gallery
---

<div class="gallery">
{% for image in site.static_files %}
  {% if image.path contains '/images/' %}
    <div class="gallery-item">
      <a href="{{ image.path | relative_url }}" data-lightbox="gallery" data-title="{{ image.name }}">
        <img src="{{ image.path | relative_url }}" alt="{{ image.name }}">
      </a>
    </div>
  {% endif %}
{% endfor %}
</div>
