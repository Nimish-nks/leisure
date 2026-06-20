---
layout: default
title: Our Tour Packages
---

<div style="text-align: center; margin-top: 50px; margin-bottom: 40px; padding: 0 15px;">
  <h2 style="color: #1e3c72; font-size: 2.2rem; margin-bottom: 15px;">Select From Our Trending Destinations Below</h2>
  <p style="color: #555; font-size: 1.1rem; max-width: 700px; margin: 0 auto; line-height: 1.6;">
    If you find a journey that speaks to you, fill out the <strong>Booking Enquiry Form</strong> at the bottom of the page or just <strong>WhatsApp</strong> us instantly! Note: the price mentioned are just to give you an idea of starting range. These can go high or low depending on requirements and market conditions. These prices consider 3 Star hotels.
  </p>
</div>

<div style="max-width: 1000px; margin: 0 auto 40px auto; background: linear-gradient(135deg, #eef2f3 0%, #8e9eab 100%); padding: 25px; border-radius: 10px; text-align: center; box-shadow: 0 4px 15px rgba(0,0,0,0.05);">
  <h3 style="color: #1e3c72; margin-top: 0; font-size: 1.4rem;">✨ Looking for something entirely unique?</h3>
  <p style="color: #333; font-size: 1rem; margin-bottom: 15px; max-width: 800px; margin-left: auto; margin-right: auto;">
    Your dream vacation shouldn't fit into a template. Whether it is a hidden gem not listed here, a personalized family milestone, or a custom solo expedition—<strong>we can curate any itinerary completely from scratch to match your budget and style!</strong>
  </p>
  <a href="#" onclick="openProtectedCustomWhatsApp(event)" style="background-color: #25D366; color: white; padding: 10px 20px; text-decoration: none; border-radius: 5px; font-weight: bold; display: inline-block; box-shadow: 0 2px 5px rgba(0,0,0,0.15);">
    💬 Customize My Trip via WhatsApp
  </a>
</div>

<div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 30px; max-width: 1100px; margin: 40px auto; padding: 0 15px;">
  {% for tour in site.data.tours %}
    <div style="border: 1px solid #ddd; padding: 0; border-radius: 12px; background: #fff; box-shadow: 0 4px 15px rgba(0,0,0,0.05); overflow: hidden; display: flex; flex-direction: column; justify-content: space-between;">
      
      <div>
        {% if tour.image %}
          <img src="{{ tour.image | relative_url }}" alt="{{ tour.title }}" style="width: 100%; height: 200px; object-fit: cover;">
        {% else %}
          <div style="width: 100%; height: 200px; background: #e1e8ed; display: flex; align-items: center; justify-content: center; color: #777;">
            🌅 No Image Available
          </div>
        {% endif %}
        
        <div style="padding: 20px;">
          <h3 style="margin-top: 0; color: #1e3c72; font-size: 1.3rem; margin-bottom: 10px;">{{ tour.title }}</h3>
          
          <div style="display: flex; justify-content: space-between; align-items: center; margin-bottom: 15px;">
            <span style="background: #f0f4f8; color: #1e3c72; font-size: 0.85rem; padding: 4px 10px; border-radius: 20px; font-weight: 600;">⏱️ {{ tour.duration }}</span>
            <span style="color: #27ae60; font-weight: bold; font-size: 1.25rem;">{{ tour.price }}</span>
          </div>
          
          <p style="color: #555; font-size: 0.95rem; line-height: 1.6; margin: 0; padding-top: 12px; border-top: 1px dashed #e1e8ed;">
            {{ tour.description }}
          </p>
        </div>
      </div>

      <div style="padding: 0 20px 20px 20px; display: grid; grid-template-columns: 1fr 1fr; gap: 10px;">
        <a href="#enquiry-form" onclick="selectTourPackage('{{ tour.title }}')" style="background-color: #1e3c72; color: white; text-align: center; padding: 11px; text-decoration: none; border-radius: 6px; font-weight: bold; font-size: 0.9rem;">Book Now</a>
        <a href="#" onclick="openProtectedTourWhatsApp(event, '{{ tour.title | escape }}')" style="background-color: #25D366; color: white; text-align: center; padding: 11px; text-decoration: none; border-radius: 6px; font-weight: bold; font-size: 0.9rem; display: flex; align-items: center; justify-content: center; gap: 4px;">WhatsApp</a>
      </div>

    </div>
  {% endfor %}
</div>

<hr style="border: 0; border-top: 1px solid #e1e8ed; margin: 40px 0;">

<div id="enquiry-form" style="padding-top: 20px;"></div>

<h2 style="text-align: center; margin-top: 50px;">Enquire Now</h2>
<p style="text-align: center; color: #666; margin-bottom: 30px;">Leave your details below, and our team will get back to you within 24 hours.</p>

<div style="width: 100%; max-width: 550px; margin: 0 auto; background: #fff; padding: 30px; border-radius: 12px; border: 1px solid #e1e8ed; box-shadow: 0 4px 15px rgba(0,0,0,0.05);">
  
  <form action="https://docs.google.com/forms/d/e/1FAIpQLScUlPRDRYVoN5_YwohDx3dGtuPJPbRGHD2-jieLBCezVyPbng/formResponse" method="POST" target="silent_submit_receiver" onsubmit="submitted=true;">
    
    <div style="margin-bottom: 20px;">
      <label style="display: block; font-weight: 600; margin-bottom: 8px; color: #1e3c72;">Name</label>
      <input type="text" name="entry.2005620554" placeholder="John Doe" required style="width: 100%; padding: 12px; border: 1px solid #ccc; border-radius: 6px; font-size: 1rem; box-sizing: border-box; outline: none; transition: border-color 0.3s;">
    </div>

    <div style="margin-bottom: 20px;">
      <label style="display: block; font-weight: 600; margin-bottom: 8px; color: #1e3c72;">Email Address</label>
      <input type="email" name="entry.1045781291" placeholder="john@example.com" required style="width: 100%; padding: 12px; border: 1px solid #ccc; border-radius: 6px; font-size: 1rem; box-sizing: border-box; outline: none;">
    </div>

    <div style="margin-bottom: 20px;">
      <label style="display: block; font-weight: 600; margin-bottom: 8px; color: #1e3c72;">Address / Location</label>
      <input type="text" name="entry.1065046570" placeholder="e.g. Delhi" required style="width: 100%; padding: 12px; border: 1px solid #ccc; border-radius: 6px; font-size: 1rem; box-sizing: border-box; outline: none;">
    </div>

    <div style="margin-bottom: 20px;">
      <label style="display: block; font-weight: 600; margin-bottom: 8px; color: #1e3c72;">Phone Number</label>
      <input type="tel" name="entry.1166974658" placeholder="+91 98765 43210" required style="width: 100%; padding: 12px; border: 1px solid #ccc; border-radius: 6px; font-size: 1rem; box-sizing: border-box; outline: none;">
    </div>

    <div style="margin-bottom: 20px;">
      <label style="display: block; font-weight: 600; margin-bottom: 8px; color: #1e3c72;">What are you interested in?</label>
      <select id="interest_dropdown" name="entry.1735697613" required style="width: 100%; padding: 12px; border: 1px solid #ccc; border-radius: 6px; font-size: 1rem; box-sizing: border-box; background: white; outline: none;">
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
      <textarea id="query_textarea" name="entry.839337160" rows="4" placeholder="Describe your travel plans or ask a question..." required style="width: 100%; padding: 12px; border: 1px solid #ccc; border-radius: 6px; font-size: 1rem; box-sizing: border-box; resize: vertical; outline: none; font-family: inherit;"></textarea>
    </div>

    <button type="submit" style="width: 100%; padding: 14px; background: linear-gradient(135deg, #1e3c72 0%, #2a5298 100%); color: white; border: none; border-radius: 6px; font-size: 1.1rem; font-weight: bold; cursor: pointer; box-shadow: 0 4px 6px rgba(0,0,0,0.1); transition: background 0.3s;">
      Send Inquiry
    </button>
  </form>
</div>

<iframe name="silent_submit_receiver" id="silent_submit_receiver" style="display:none;" onload="handleFormConfirmation();"></iframe>

<script>
  function selectTourPackage(packageName) {
    var dropdown = document.getElementById('interest_dropdown');
    var queryBox = document.getElementById('query_textarea');
    
    if (dropdown) {
      dropdown.value = "Tour package"; 
    }
    if (queryBox) {
      queryBox.value = "Hi, I am interested in booking your '" + packageName + "' package. Please share details and customize the plan for us.";
    }
  }

  // Decodes phone number on-the-fly for package cards
  function openProtectedTourWhatsApp(event, tourTitle) {
    event.preventDefault();
    var secretKey = 'OTE3Mjg5MDM2NjQ1'; // Hidden phone identifier
    var realNumber = atob(secretKey);
    var textMessage = encodeURIComponent("Hi! I'm interested in the " + tourTitle + " package.");
    window.open("https://wa.me/" + realNumber + "?text=" + textMessage, '_blank');
  }

  // Decodes phone number on-the-fly for custom banner
  function openProtectedCustomWhatsApp(event) {
    event.preventDefault();
    var secretKey = 'OTE3Mjg5MDM2NjQ1'; 
    var realNumber = atob(secretKey);
    var textMessage = encodeURIComponent("Hi! I'm looking for a completely unique customized itinerary.");
    window.open("https://wa.me/" + realNumber + "?text=" + textMessage, '_blank');
  }

  var submitted = false;
  function handleFormConfirmation() {
    if (submitted) {
      alert('Thank you! Your enquiry has been submitted successfully.');
      window.location.reload();
    }
  }
</script>
