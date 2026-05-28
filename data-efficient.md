---
layout: page
title: Data-Efficient Geotechnical Modelling
permalink: /data-efficient/
---

## Data-Efficient Geotechnical Modelling

Geotechnical data are often sparse, uncertain, site-dependent, and expensive to obtain. Our work develops data-efficient probabilistic modelling frameworks for reliable soil property prediction under limited data conditions.

The main idea is to combine abundant low-fidelity data with a few informative high-fidelity site-specific measurements selected through active learning. This enables accurate and reliable quasi-site-specific prediction of soil parameters with reduced data demand.

---

<style>
  .de-tabs {
    display: flex;
    flex-direction: row;
    gap: 20px;
    margin-top: 25px;
    margin-bottom: 30px;
  }

  .de-tab {
    flex: 1;
    border: 2px solid #222;
    padding: 20px 12px;
    text-align: center;
    cursor: pointer;
    background-color: #ffffff;
    transition: background-color 0.2s ease, border-color 0.2s ease;
  }

  .de-tab:hover {
    background-color: #f0f8ff;
  }

  .de-tab.active {
    background-color: #dff1ff;
    border-color: #4a90c2;
  }

  .de-tab h3 {
    margin: 0;
    font-size: 20px;
  }

  .de-content {
    display: none;
    border-top: 2px solid #ddd;
    padding-top: 25px;
    margin-top: 10px;
  }

  .de-content.active {
    display: block;
  }

  @media screen and (max-width: 700px) {
    .de-tabs {
      flex-direction: column;
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

**Active Learning based Multi-fidelity Residual Gaussian Process** is designed for data-efficient geomaterial property prediction.

This framework combines abundant low-fidelity data with sparse site-specific high-fidelity data. A low-fidelity model first provides preliminary estimations, and active learning then selects informative high-fidelity observations to calibrate the residual model.

**Main features:**

- Multi-fidelity residual modelling
- Active learning for informative high-fidelity data acquisition
- Gaussian-process-based probabilistic prediction
- Quasi-site-specific soil property modelling
- Reduced demand for expensive site-specific measurements

</div>

<div id="ki-de-nn" class="de-content">

### KI-DE-NN

**Knowledge-Informed Data-Efficient Neural Network** focuses on developing robust soil correlations under sparse and noisy data conditions.

This framework integrates active learning, knowledge-informed neural network constraints, and uncertainty quantification to improve the reliability and practicality of data-driven soil correlation modelling.

**Main features:**

- Knowledge-informed neural network architecture
- Positive-output constraint for physically meaningful predictions
- Active learning for compact informative datasets
- Monte Carlo dropout for uncertainty quantification
- Efficient prediction of soil compression-related parameters

</div>

<div id="pod-gpr" class="de-content">

### POD-GPR

**Proper Orthogonal Decomposition Gaussian Process Regression** provides a reduced-order probabilistic modelling strategy for efficient geotechnical prediction.

This framework combines dimensionality reduction with Gaussian-process-based uncertainty quantification, enabling efficient prediction when model outputs are high-dimensional or spatially distributed.

**Main features:**

- Proper orthogonal decomposition for reduced-order representation
- Gaussian process regression for probabilistic prediction
- Efficient modelling of high-dimensional geotechnical responses
- Uncertainty-aware prediction
- Potential applications in spatial soil property modelling and digital geotechnics

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
