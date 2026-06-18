---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
---
## Our Featured Tour Packages

<div style="display: flex; gap: 20px; flex-wrap: wrap; margin-top: 20px;">
  {% for tour in site.data.tours %}
    <div style="flex: 1; min-width: 250px; border: 1px solid #ddd; padding: 20px; border-radius: 8px; background: #f9f9f9; box-shadow: 0 4px 6px rgba(0,0,0,0.05);">
      <h3>{{ tour.title }}</h3>
      <p><strong>Duration:</strong> {{ tour.duration }}</p>
      <p>{{ tour.description }}</p>
      <p style="color: #27ae60; font-weight: bold; font-size: 1.2em;">{{ tour.price }}</p>
    </div>
  {% endfor %}
</div>
