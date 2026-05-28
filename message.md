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
    padding: 10px;
    box-shadow: 0 2px 8px rgba(0,0,0,0.05);
    overflow: hidden;
  }

  .google-form-frame {
    width: 100%;
    height: 850px;
    border: none;
  }

  @media screen and (max-width: 800px) {
    .contact-wrapper {
      flex-direction: column;
      gap: 30px;
    }

    .contact-left h1 {
      font-size: 34px;
    }

    .google-form-frame {
      height: 950px;
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
    <iframe
      class="google-form-frame"
      src="https://docs.google.com/forms/d/e/1FAIpQLSffcFS0nUp8XdwvlRyxnaOo-Pc6zGU-MqPrXJ3SbXo9j0okLA/viewform?embedded=true"
      frameborder="0"
      marginheight="0"
      marginwidth="0">
      Loading…
    </iframe>
  </div>

</div>
