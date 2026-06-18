---
layout: default
title: Our Tour Packages
---

## Explore Our Curated Packages

Select from our trending destinations below. If you find a journey that speaks to you, fill out the booking enquiry form at the bottom of the page!

<!-- Tour Packages Grid Container -->
<div style="display: flex; gap: 20px; flex-wrap: wrap; margin-top: 20px; margin-bottom: 40px;">
  {% for tour in site.data.tours %}
    <div style="flex: 1; min-width: 280px; border: 1px solid #ddd; padding: 0; border-radius: 8px; background: #fff; box-shadow: 0 4px 6px rgba(0,0,0,0.05); overflow: hidden; display: flex; flex-direction: column;">
      
      <!-- Tour Image Section -->
      {% if tour.image %}
        <img src="{{ tour.image | relative_url }}" alt="{{ tour.title }}" style="width: 100%; height: 200px; object-fit: cover;">
      {% else %}
        <!-- Fallback placeholder background if an image is missing -->
        <div style="width: 100%; height: 200px; background: #e1e8ed; display: flex; align-items: center; justify-content: center; color: #777;">
          🌅 No Image Available
        </div>
      {% endif %}
      
      <!-- Tour Text Content Section -->
      <div style="padding: 20px; flex-grow: 1; display: flex; flex-direction: column; justify-content: space-between;">
        <div>
          <h3 style="margin-top: 0; color: #1e3c72; font-size: 1.4rem;">{{ tour.title }}</h3>
          <p style="margin: 5px 0; color: #555;"><strong>Duration:</strong> {{ tour.duration }}</p>
          <p style="color: #666; font-size: 0.95rem; line-height: 1.5;">{{ tour.description }}</p>
        </div>
        <p style="color: #27ae60; font-weight: bold; font-size: 1.3em; margin-bottom: 0; margin-top: 15px;">{{ tour.price }}</p>
      </div>

    </div>
  {% endfor %}
</div>

<hr style="border: 0; border-top: 1px solid #e1e8ed; margin: 40px 0;">
<!-- Booking Enquiry Form Section -->
<h2>Enquire Now</h2>
<p>Ready to book or have questions? Let us know which package interests you, and our team will reach out within 24 hours.</p>

<div style="width: 100%; max-width: 650px; margin: 20px auto 0 auto; overflow: hidden; border-radius: 8px; border: 1px solid #ddd; box-shadow: 0 4px 6px rgba(0,0,0,0.05);">
  <!-- REMEMBER: Replace the placeholder below with your real Google Forms link -->
  <iframe src="https://docs.google.com/forms/d/e/1FAIpQLScUlPRDRYVoN5_YwohDx3dGtuPJPbRGHD2-jieLBCezVyPbng/viewform?embedded=true" width="640" height="1359" frameborder="0" marginheight="0" marginwidth="0">Loading…</iframe>
</div>
