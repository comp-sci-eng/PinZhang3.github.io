---
layout: page
title: Contact
permalink: /contact/
weight: 8
---

<style>
  .contact-wrapper {
    display: flex;
    gap: 60px;
    align-items: flex-start;
    margin-top: 40px;
  }

  .contact-left {
    flex: 1;
  }

  .contact-left .tag {
    display: inline-block;
    border: 1px solid #ddd;
    border-radius: 20px;
    padding: 6px 14px;
    font-size: 14px;
    margin-bottom: 25px;
  }

  .contact-left h1 {
    font-size: 44px;
    line-height: 1.1;
    margin-bottom: 25px;
  }

  .contact-left p {
    font-size: 17px;
    color: #555;
    line-height: 1.5;
  }

  .contact-form-box {
    flex: 1.4;
    border: 1px solid #ddd;
    border-radius: 10px;
    padding: 25px;
    box-shadow: 0 2px 8px rgba(0,0,0,0.05);
  }

  .form-row {
    display: flex;
    gap: 15px;
  }

  .form-group {
    flex: 1;
    margin-bottom: 18px;
  }

  .form-group label {
    display: block;
    font-weight: 600;
    margin-bottom: 8px;
  }

  .form-group input,
  .form-group textarea {
    width: 100%;
    box-sizing: border-box;
    border: 1px solid #ddd;
    border-radius: 8px;
    padding: 12px;
    font-size: 15px;
  }

  .form-group textarea {
    height: 220px;
    resize: vertical;
  }

  .send-button {
    width: 100%;
    background-color: #168bf2;
    color: white;
    border: none;
    border-radius: 8px;
    padding: 15px;
    font-size: 16px;
    cursor: pointer;
  }

  .send-button:hover {
    background-color: #0f76cc;
  }

  @media screen and (max-width: 800px) {
    .contact-wrapper {
      flex-direction: column;
      gap: 30px;
    }

    .form-row {
      flex-direction: column;
      gap: 0;
    }

    .contact-left h1 {
      font-size: 34px;
    }
  }
</style>

<div class="contact-wrapper">

  <div class="contact-left">
    <div class="tag">✈ Contact Us</div>

    <h1>We’d Love to<br>Hear from You<br>and Connect</h1>

    <p>
      We welcome enquiries about research collaboration, student opportunities,
      visiting positions, and data-efficient geotechnical modelling.
    </p>
  </div>

  <div class="contact-form-box">
    <form onsubmit="sendMail(event)">
      <div class="form-row">
        <div class="form-group">
          <label>First Name *</label>
          <input type="text" id="firstName" placeholder="Jane" required>
        </div>

        <div class="form-group">
          <label>Last Name *</label>
          <input type="text" id="lastName" placeholder="Smith" required>
        </div>
      </div>

      <div class="form-group">
        <label>Email *</label>
        <input type="email" id="email" placeholder="jane@example.com" required>
      </div>

      <div class="form-group">
        <label>Message</label>
        <textarea id="message" placeholder="Write your message here"></textarea>
      </div>

      <button type="submit" class="send-button">Send Message</button>
    </form>
  </div>

</div>

<script>
  function sendMail(event) {
    event.preventDefault();

    var firstName = document.getElementById("firstName").value;
    var lastName = document.getElementById("lastName").value;
    var email = document.getElementById("email").value;
    var message = document.getElementById("message").value;

    var recipient = "pinzhang@nus.edu.sg";
    var subject = "Website Contact Form Message";
    var body =
      "Name: " + firstName + " " + lastName + "%0D%0A" +
      "Email: " + email + "%0D%0A%0D%0A" +
      "Message:%0D%0A" + encodeURIComponent(message);

    window.location.href = "mailto:" + recipient + "?subject=" + encodeURIComponent(subject) + "&body=" + body;
  }
</script>
