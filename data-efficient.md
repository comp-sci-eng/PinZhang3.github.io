---
layout: page
title: Data-Efficient Geotechnical Modelling
permalink: /data-efficient/
---

## Data-Efficient Geotechnical Modelling

Geotechnical data are often sparse, uncertain, site-dependent, and expensive to obtain. Our work develops data-efficient probabilistic modelling frameworks for reliable soil property prediction under limited data conditions.

---

<style>
  .de-tabs {
    display: flex;
    flex-direction: row;
    gap: 14px;
    margin-top: 28px;
    margin-bottom: 34px;
    padding: 8px;
    background: #f7f9fb;
    border: 1px solid #e5eaf0;
    border-radius: 16px;
  }

  .de-tab {
    flex: 1;
    padding: 16px 14px;
    text-align: center;
    cursor: pointer;
    background-color: #ffffff;
    border: 1px solid #d9e2ec;
    border-radius: 12px;
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
    font-size: 19px;
    font-weight: 700;
    letter-spacing: 0.3px;
  }

  .de-content {
    display: none;
    border-top: 1px solid #e5eaf0;
    padding-top: 26px;
    margin-top: 10px;
  }

  .de-content.active {
    display: block;
  }

  .de-section-title {
    margin-top: 0;
    margin-bottom: 18px;
  }

  .de-info-bar {
    display: flex;
    flex-wrap: wrap;
    gap: 14px;
    align-items: stretch;
    margin: 18px 0 22px 0;
  }

  .de-info-card {
    flex: 1;
    min-width: 240px;
    border: 1px solid #d9e2ec;
    border-radius: 12px;
    padding: 14px 16px;
    background-color: #fbfdff;
  }

  .de-info-card strong {
    display: block;
    margin-bottom: 6px;
    font-size: 15px;
  }

  .de-info-card a {
    color: #1a73b8;
    text-decoration: none;
  }

  .de-info-card a:hover {
    text-decoration: underline;
  }

  .de-method-img {
    display: block;
    width: 88%;
    max-width: 900px;
    margin: 24px auto 30px auto;
    border: 1px solid #ddd;
    border-radius: 8px;
  }

  @media screen and (max-width: 700px) {
    .de-tabs {
      flex-direction: column;
    }

    .de-method-img {
      width: 100%;
    }
  }
</style>

<div class="de-tabs">

  <div class="de-tab active" onclick="showDESection('al-mr-gp', this)">
    <h3>AL-MR-GP</h3>
  </div>

  <div class="de-tab" onclick="showDESection('ki-de-nn', this)">
    <h3>KI-DE-NN</h3>
  </div>

  <div class="de-tab" onclick="showDESection('pod-gpr', this)">
    <h3>POD-GPR</h3>
  </div>

</div>

<div id="al-mr-gp" class="de-content active">

### AL-MR-GP

<div class="de-info-bar">
  <div class="de-info-card">
    <strong>Theory</strong>
    <a href="#">Add theory link here</a>
  </div>

  <div class="de-info-card">
    <strong>Related paper</strong>
    <a href="#">Add paper link here</a>
  </div>
</div>

<img src="{{ '/assets/research/AL-MR-GP.png' | relative_url }}" alt="AL-MR-GP framework" class="de-method-img">

</div>

<div id="ki-de-nn" class="de-content">

### KI-DE-NN

<div class="de-info-bar">
  <div class="de-info-card">
    <strong>Theory</strong>
    <a href="#">Add theory link here</a>
  </div>

  <div class="de-info-card">
    <strong>Related paper</strong>
    <a href="#">Add paper link here</a>
  </div>
</div>

<img src="{{ '/assets/research/KI-DE-NN.png' | relative_url }}" alt="KI-DE-NN framework" class="de-method-img">

</div>

<div id="pod-gpr" class="de-content">

### POD-GPR

<div class="de-info-bar">
  <div class="de-info-card">
    <strong>Theory</strong>
    <a href="#">Add theory link here</a>
  </div>

  <div class="de-info-card">
    <strong>Related paper</strong>
    <a href="#">Add paper link here</a>
  </div>
</div>

<img src="{{ '/assets/research/POD-GPR1.png' | relative_url }}" alt="POD-GPR framework" class="de-method-img">

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
