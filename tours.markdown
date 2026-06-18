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
<h2 style="text-align: center; margin-top: 50px;">Enquire Now</h2>
<p style="text-align: center; color: #666; margin-bottom: 30px;">Leave your details below, and our team will get back to you within 24 hours.</p>

<div style="width: 100%; max-width: 550px; margin: 0 auto; background: #fff; padding: 30px; border-radius: 12px; border: 1px solid #e1e8ed; box-shadow: 0 4px 15px rgba(0,0,0,0.05);">
  
  <form action="https://docs.google.com/forms/u/0/d/11fraCaDA3U0KD15KiL3-Xsn8J6dgNSPegE-x6T4mhr0/formResponse" method="POST" target="_hidden_iframe">
    
    <div style="margin-bottom: 20px;">
      <label style="display: block; font-weight: 600; margin-bottom: 8px; color: #1e3c72;">Name</label>
      <input type="text" name="entry.2005620554" placeholder="John Doe" required style="width: 100%; padding: 12px; border: 1px solid #ccc; border-radius: 6px; font-size: 1rem; box-sizing: border-box; outline: none; transition: border-color 0.3s;">
    </div>

    <div style="margin-bottom: 20px;">
      <label style="display: block; font-weight: 600; margin-bottom: 8px; color: #1e3c72;">Email Address</label>
      <input type="email" name="entry.1045781291" placeholder="john@example.com" required style="width: 100%; padding: 12px; border: 1px solid #ccc; border-radius: 6px; font-size: 1rem; box-sizing: border-box; outline: none;">
    </div>

    <div style="margin-bottom: 20px;">
      <label style="display: block; font-weight: 600; margin-bottom: 8px; color: #1e3c72;">Phone Number</label>
      <input type="tel" name="entry.1065046570" placeholder="+91 98765 43210" required style="width: 100%; padding: 12px; border: 1px solid #ccc; border-radius: 6px; font-size: 1rem; box-sizing: border-box; outline: none;">
    </div>

    <div style="margin-bottom: 20px;">
      <label style="display: block; font-weight: 600; margin-bottom: 8px; color: #1e3c72;">What are you interested in?</label>
      <select name="entry.1166974658" required style="width: 100%; padding: 12px; border: 1px solid #ccc; border-radius: 6px; font-size: 1rem; box-sizing: border-box; background: white; outline: none;">
        <option value="" disabled selected>Select an option...</option>
        <option value="Tour package">Tour package</option>
        <option value="Hotel booking">Hotel booking</option>
        <option value="Domestic Flight Tickets">Domestic Flight Tickets</option>
        <option value="International Flight Tickets">International Flight Tickets</option>
        <option value="Visa Consultancy">Visa Consultancy</option>
      </select>
    </div>

    <div style="margin-bottom: 25px;">
      <label style="display: block; font-weight: 600; margin-bottom: 8px; color: #1e3c72;">Query</label>
      <textarea name="entry.839337160" rows="4" placeholder="Describe your travel plans or ask a question..." required style="width: 100%; padding: 12px; border: 1px solid #ccc; border-radius: 6px; font-size: 1rem; box-sizing: border-box; resize: vertical; outline: none; font-family: inherit;"></textarea>
    </div>

    <button type="submit" style="width: 100%; padding: 14px; background: linear-gradient(135deg, #1e3c72 0%, #2a5298 100%); color: white; border: none; border-radius: 6px; font-size: 1.1rem; font-weight: bold; cursor: pointer; box-shadow: 0 4px 6px rgba(0,0,0,0.1); transition: background 0.3s;">
      Send Inquiry
    </button>
  </form>
</div>

<iframe name="_hidden_iframe" id="_hidden_iframe" style="display:none;" onload="if(submitted) { alert('Thank you! Your enquiry has been submitted successfully.'); window.location.reload(); }"></iframe>

<script>var submitted=false;</script>
<script>
  document.querySelector('form').addEventListener('submit', function() {
    submitted = true;
  });
</script>
