---
layout: page
title: "Terminology"
permalink: /terminology/
nav: true
nav_order: 2
---

The **HL7 Lithuania Terminology Registry** provides access to code systems, value sets, and mappings that support all Lithuanian FHIR Implementation Guides.  
These terminology resources ensure **semantic consistency** and **interoperability** across healthcare systems.

<div class="term-grid">

  <div class="term-card">
    <div class="term-image" style="background-image: url('{{ '/assets/img/termservice.png' | relative_url }}');"></div>
    <div class="term-content">
      <h3>Terminology Services</h3>
      <p>API-based access to Lithuanian FHIR terminology resources and validation tools.</p>
      <a href="https://htx.hl7.lt" class="term-link" target="_blank">Open Service</a>
    </div>
  </div>

  <div class="term-card">
    <div class="term-image" style="background-image: url('{{ '/assets/img/codesystem.png' | relative_url }}');"></div>
    <div class="term-content">
      <h3>Code Systems</h3>
      <p>National and domain-specific code systems used across Lithuanian FHIR profiles.</p>
      <a href="https://tx.hl7.lt/fhir/CodeSystem/" class="term-link" target="_blank">View Repository</a>
    </div>
  </div>

  <div class="term-card">
    <div class="term-image" style="background-image: url('{{ '/assets/img/valueset.png' | relative_url }}');"></div>
    <div class="term-content">
      <h3>Value Sets</h3>
      <p>Standardized collections of codes representing clinical and administrative concepts.</p>
      <a href="https://tx.hl7.lt/fhir/ValueSet" class="term-link" target="_blank">View Repository</a>
    </div>
  </div>

  <div class="term-card">
    <div class="term-image" style="background-image: url('{{ '/assets/img/conceptmap.png' | relative_url }}');"></div>
    <div class="term-content">
      <h3>Concept Maps</h3>
      <p>Mappings between Lithuanian and international terminologies such as SNOMED CT, LOINC, and ICD-10.</p>
      <a href="https://tx.hl7.lt/fhir/ConceptMap" class="term-link" target="_blank">View Repository</a>
    </div>
  </div>

</div>

---

### External References

- [HL7 FHIR Terminology Service](https://build.fhir.org/terminology-service.html)
- [FHIR ValueSet Resource](https://hl7.org/fhir/valueset.html)
- [FHIR CodeSystem Resource](https://hl7.org/fhir/codesystem.html)