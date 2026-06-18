---
layout: default
title: Customer Testimonials
---

## What Our Travelers Say

Don't just take our word for it. Here are real stories from real travelers who explored the world with us.

<div style="display: flex; flex-direction: column; gap: 25px; margin-top: 20px;">
  {% for review in site.data.testimonials %}
    <div style="background: #fff; padding: 25px; border-radius: 8px; box-shadow: 0 4px 6px rgba(0,0,0,0.05); display: flex; gap: 20px; align-items: flex-start; border: 1px solid #e1e8ed;">
      
      <!-- Customer Avatar Section -->
      {% if review.avatar %}
        <img src="{{ review.avatar | relative_url }}" alt="{{ review.name }}" style="width: 70px; height: 70px; border-radius: 50%; object-fit: cover; border: 2px solid #1e3c72; flex-shrink: 0;">
      {% else %}
        <!-- Fallback initials/placeholder avatar if image is missing -->
        <div style="width: 70px; height: 70px; border-radius: 50%; background: #e1e8ed; display: flex; align-items: center; justify-content: center; font-size: 1.5rem; color: #777; flex-shrink: 0; border: 2px solid #ccc;">
          👤
        </div>
      {% endif %}

      <!-- Review Text Content Section -->
      <div style="flex-grow: 1;">
        <div style="color: #f1c40f; font-size: 1rem; margin-bottom: 8px;">{{ review.rating }}</div>
        <p style="font-style: italic; font-size: 1.05rem; color: #444; margin: 0 0 15px 0; line-height: 1.5;">"{{ review.quote }}"</p>
        
        <div>
          <strong style="color: #1e3c72; font-size: 1.1rem; display: block;">{{ review.name }}</strong>
          <span style="font-size: 0.85rem; color: #777;">{{ review.location }}</span>
        </div>
      </div>

    </div>
  {% endfor %}
</div>
