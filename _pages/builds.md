---
layout: page
permalink: /builds-home/
title: "Builds"
nav: true
nav_order: 1
---

<div class="builds-grid">

  <div class="build-card">
    <div class="build-image" style="background-image: url('{{ '/assets/img/base.png' | relative_url }}');"></div>
    <div class="build-content">
      <h3>LT Base</h3>
      <p>Core Lithuanian FHIR Implementation Guide with foundational profiles and terminology.</p>
      <div class="build-buttons">
        <a href="https://build.fhir.org/ig/HL7LT/ig-lt-base" target="_blank" class="build-link">Latest Build</a>
        <a href="https://hl7.lt/fhir/base/history.html" target="_blank" class="build-link secondary">History</a>
      </div>
    </div>
  </div>

  <div class="build-card">
    <div class="build-image" style="background-image: url('{{ '/assets/img/vitalsigns.png' | relative_url }}');"></div>
    <div class="build-content">
      <h3>Vital Signs</h3>
      <p>Standardized observation structures for clinical vital signs data.</p>
      <div class="build-buttons">
        <a href="https://build.fhir.org/ig/HL7LT/ig-lt-vitalsigns" target="_blank" class="build-link">Latest Build</a>
        <a href="https://hl7.lt/fhir/vitalsigns/history.html" target="_blank" class="build-link secondary">History</a>
      </div>
    </div>
  </div>

  <div class="build-card">
    <div class="build-image" style="background-image: url('{{ '/assets/img/lab.png' | relative_url }}');"></div>
    <div class="build-content">
      <h3>LT Lab</h3>
      <p>FHIR profiles and resources for laboratory observations and results.</p>
      <div class="build-buttons">
        <a href="https://build.fhir.org/ig/HL7LT/ig-lt-lab/en/" target="_blank" class="build-link">
          Latest Build
        </a>
        <a href="#" class="build-link secondary disabled">
          History
        </a>
      </div>
    </div>
  </div>

  <div class="build-card">
    <div class="build-image" style="background-image: url('{{ '/assets/img/lifestyle.png' | relative_url }}');"></div>
    <div class="build-content">
      <h3>Life Style</h3>
      <p>Guidelines for lifestyle-related health indicators and patient records.</p>
      <div class="build-buttons">
        <a href="https://build.fhir.org/ig/HL7LT/ig-lt-lifestyle" target="_blank" class="build-link">Latest Build</a>
        <a href="https://hl7.lt/fhir/lifestyle/history.html" target="_blank" class="build-link secondary">History</a>
      </div>
    </div>
  </div>

  <div class="build-card">
    <div class="build-image" style="background-image: url('{{ '/assets/img/screening.png' | relative_url }}');"></div>
    <div class="build-content">
      <h3>Screening</h3>
      <p>Implementation Guide for preventive healthcare and immunization tracking.</p>
      <div class="build-buttons">
        <a href="#" class="build-link disabled">Coming Soon</a>
      </div>
    </div>
  </div>

  <div class="build-card">
    <div class="build-image" style="background-image: url('{{ '/assets/img/breast.png' | relative_url }}');"></div>
    <div class="build-content">
      <h3>Breast Diagnostic</h3>
      <p>FHIR Implementation Guide supporting breast diagnostics and structured clinical data.</p>
      <div class="build-buttons">
        <a href="https://build.fhir.org/ig/HL7LT/ig-lt-breast" target="_blank" class="build-link">
          Latest Build
        </a>
        <a href="https://hl7.lt/fhir/breast/history.html" target="_blank" class="build-link secondary">
          History
        </a>
      </div>
    </div>
  </div>

<div class="build-card">
  <div class="build-image" style="background-image: url('{{ '/assets/img/prostate.png' | relative_url }}');"></div>
  <div class="build-content">
    <h3>Prostate Cancer</h3>
    <p>FHIR Implementation Guide supporting prostate diagnostics and structured clinical data.</p>
    <div class="build-buttons">
      <a href="https://build.fhir.org/ig/HL7LT/ig-lt-prostate" target="_blank" class="build-link">
        Latest Build
      </a>
      <!-- Add history later when available -->
      <!--
      <a href="https://hl7.lt/fhir/prostate/history.html" target="_blank" class="build-link secondary">
        History
      </a>
      -->
    </div>
  </div>
</div>


  <div class="build-card">
    <div class="build-image" style="background-image: url('{{ '/assets/img/lungs.png' | relative_url }}');"></div>
    <div class="build-content">
      <h3>Lung Cancer</h3>
      <p>FHIR Implementation Guide for structured lung cancer diagnostics and care pathways.</p>
      <div class="build-buttons">
        <a href="#" class="build-link disabled">Coming Soon</a>
      </div>
    </div>
  </div>

  <div class="build-card">
    <div class="build-image" style="background-image: url('{{ '/assets/img/cervical.png' | relative_url }}');"></div>
    <div class="build-content">
      <h3>Cervical Cancer</h3>
      <p>FHIR profiles supporting cervical cancer screening and diagnostic workflows.</p>
      <div class="build-buttons">
        <a href="#" class="build-link disabled">Coming Soon</a>
      </div>
    </div>
  </div>

  <div class="build-card">
    <div class="build-image" style="background-image: url('{{ '/assets/img/colorectal.png' | relative_url }}');"></div>
    <div class="build-content">
      <h3>Colorectal Cancer</h3>
      <p>FHIR Implementation Guide for colorectal cancer screening, diagnostics, and reporting.</p>
      <div class="build-buttons">
        <a href="#" class="build-link disabled">Coming Soon</a>
      </div>
    </div>
  </div>

</div>

<style>
.build-buttons {
  display: flex;
  gap: 0.5rem;
  margin-top: 0.8rem;
}

.build-link.secondary {
  background-color: #fff;
  color: #117880;
  border: 2px solid #117880;
  transition: all 0.2s ease-in-out;
}

.build-link.secondary:hover {
  background-color: #6cc9beff;
  color: #fff;
}
</style>
