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


   <!-- Floating WhatsApp Button -->
   <a href="https://wa.me/917289036645?text=Hi!%20I%20want%20to%20know%20more%20about%20your%20tours." 
      target="_blank" 
      rel="noopener noreferrer"
      style="position: fixed; width: 60px; height: 60px; bottom: 40px; right: 40px; background-color: #25d366; color: white; border-radius: 50px; text-align: center; font-size: 30px; box-shadow: 2px 2px 3px #999; z-index: 100; display: flex; align-items: center; justify-content: center; text-decoration: none; transition: transform 0.3s ease;">
       💬
   </a>
