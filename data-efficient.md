---
layout: page
title: Data-Efficient Geotechnical Modelling
permalink: /data-efficient/
---

<style>
  .de-tabs {
    display: flex;
    flex-direction: row;
    gap: 14px;
    margin-top: 20px;
    margin-bottom: 34px;
    padding: 8px;
    background: #f7f9fb;
    border: 1px solid #e5eaf0;
    border-radius: 18px;
  }

  .de-tab {
    flex: 1;
    padding: 16px 14px;
    text-align: center;
    cursor: pointer;
    background-color: #ffffff;
    border: 1px solid #d9e2ec;
    border-radius: 14px;
    box-shadow: 0 2px 8px rgba(0,0,0,0.04);
    transition: all 0.2s ease;
  }

  .de-tab:hover {
    background-color: #eef7ff;
    border-color: #8bbce8;
    transform: translateY(-1px);
    box-shadow: 0 4px 12px rgba(0,0,0,0.08);
  }

  .de-tab.active {
    background-color: #dff1ff;
    border-color: #4a90c2;
    box-shadow: 0 4px 14px rgba(74,144,194,0.22);
  }

  .de-tab h3 {
    margin: 0;
    font-size: 20px;
    font-weight: 700;
    letter-spacing: 0.3px;
  }

  .de-content {
    display: none;
    border-top: 1px solid #e5eaf0;
    padding-top: 30px;
    margin-top: 10px;
  }

  .de-content.active {
    display: block;
  }

  .de-case-row {
    display: flex;
    flex-direction: row;
    gap: 34px;
    align-items: center;
    margin-top: 10px;
    margin-bottom: 35px;
  }

  .de-case-image {
    flex: 1.1;
  }

  .de-case-image img {
    display: block;
    width: 100%;
    max-width: 620px;
    border: 1px solid #ddd;
    border-radius: 10px;
  }

  .de-case-text {
    flex: 1;
    font-size: 16px;
    line-height: 1.65;
    color: #333;
  }

  .de-case-text p {
    margin-top: 0;
    margin-bottom: 18px;
  }

  .de-links {
    margin-top: 18px;
    font-size: 15px;
  }

  .de-links a {
    color: #1a73b8;
    text-decoration: none;
    font-weight: 600;
  }

  .de-links a:hover {
    text-decoration: underline;
  }

  @media screen and (max-width: 800px) {
    .de-tabs {
      flex-direction: column;
    }

    .de-case-row {
      flex-direction: column;
      align-items: flex-start;
    }

    .de-case-image img {
      max-width: 100%;
    }
  }
</style>

<div class="de-tabs">

  <div class="de-tab active" onclick="showDESection('geo-data', this)">
    <h3>Geo-data</h3>
  </div>

  <div class="de-tab" onclick="showDESection('tunneling', this)">
    <h3>Tunneling</h3>
  </div>

</div>

<div id="geo-data" class="de-content active">

  <div class="de-case-row">

    <div class="de-case-image">
      <img src="{{ '/assets/research/KI-DE.png' | relative_url }}" alt="KI-DE framework">
    </div>

    <div class="de-case-text">
      <p>
        <strong>KIDE theory:</strong> A Knowledge-Informed Data-Efficient framework that maximises the value of sparse, noisy, and uncertain geotechnical data while preserving engineering realism and predictive reliability.
      </p>

      <div class="de-links">
        Paper <a href="#">[link]</a>; 
        Code <a href="#">[link]</a>; 
        Software <a href="#">[link]</a>
      </div>
    </div>

  </div>

</div>

<div id="tunneling" class="de-content">

  <div class="de-case-row">

    <div class="de-case-image">
      <!-- Add tunneling image here later -->
      <!-- Example:
      <img src="{{ '/assets/research/tunneling-image.png' | relative_url }}" alt="Tunneling framework">
      -->
    </div>

    <div class="de-case-text">
      <p>
        <strong>Tunneling:</strong> Add tunneling-related description here.
      </p>

      <div class="de-links">
        Paper <a href="#">[link]</a>; 
        Code <a href="#">[link]</a>; 
        Software <a href="#">[link]</a>
      </div>
    </div>

  </div>

</div>

<script>
  function showDESection(sectionId, clickedTab) {
    var contents = document.querySelectorAll('.de-content');
    var tabs = document.querySelectorAll('.de-tab');

    contents.forEach(function(content) {
      content.classList.remove('active');
    });

    tabs.forEach(function(tab) {
      tab.classList.remove('active');
    });

    document.getElementById(sectionId).classList.add('active');
    clickedTab.classList.add('active');
  }
</script>
