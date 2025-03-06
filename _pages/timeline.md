---
layout: page
title: research timeline
permalink: /timeline/
description: A chronological overview of my research journey and key milestones.
nav: true
nav_order: 5
---

<div class="timeline">
  <div class="container left">
    <div class="date">2024</div>
    <i class="icon fa fa-microscope"></i>
    <div class="content">
      <h2>Postdoctoral Researcher at UC Berkeley/HHMI</h2>
      <p>Investigating viral genome packaging mechanisms in Prof. Carlos J. Bustamante's lab, focusing on how viral ATPase motors generate mechanical force to package DNA.</p>
      <p><strong>Key Publication:</strong> "Mapping Fast DNA Polymerase Exchange during Replication" in Nature Communications</p>
    </div>
  </div>
  <div class="container right">
    <div class="date">2023</div>
    <i class="icon fa fa-dna"></i>
    <div class="content">
      <h2>Research on DNA-Protein Interactions</h2>
      <p>Published findings on T7 Gp2.5 binding dynamics and single-stranded DNA binding protein coordination in DNA metabolism.</p>
      <p><strong>Key Publications:</strong></p>
      <ul>
        <li>"Regulation of T7 Gp2.5 Binding Dynamics by Its C-Terminal Tail, Template Conformation and Sequence" in Nucleic Acids Research</li>
        <li>"Unravelling How Single-Stranded DNA Binding Protein Coordinates DNA Metabolism Using Single-Molecule Approaches" in International Journal of Molecular Sciences</li>
      </ul>
    </div>
  </div>
  <div class="container left">
    <div class="date">2017-2022</div>
    <i class="icon fa fa-graduation-cap"></i>
    <div class="content">
      <h2>PhD and Postdoctoral Training at VU Amsterdam</h2>
      <p>Developed and applied correlated optical tweezers and fluorescence microscopy to observe replication dynamics at higher resolution using a simplified T7 system.</p>
      <p><strong>Research Focus:</strong> Decentralized model of DNA replication, challenging previous assumptions about replication dynamics.</p>
    </div>
  </div>
  <div class="container right">
    <div class="date">2017</div>
    <i class="icon fa fa-flask"></i>
    <div class="content">
      <h2>Publications from Master's Research at UCAS</h2>
      <p>Published findings on novel long-acting biopharmaceuticals through PEGylation and albumin-binding domains.</p>
      <p><strong>Key Publications:</strong></p>
      <ul>
        <li>"Oxidized Catechol-Derived Poly(Ethylene Glycol) for Thiol-Specific Conjugation" in Reactive and Functional Polymers</li>
        <li>"Purification and Characterization of a Long-Acting Ciliary Neurotrophic Factor via Genetically Fused with an Albumin-Binding Domain" in Protein Expression and Purification</li>
      </ul>
    </div>
  </div>
  <div class="container left">
    <div class="date">Prior to 2017</div>
    <i class="icon fa fa-university"></i>
    <div class="content">
      <h2>MSc at University of the Chinese Academy of Sciences</h2>
      <p>Studied under Professors Zhiguo Su and Yongdong Liu, focusing on novel long-acting biopharmaceuticals.</p>
      <p><strong>Research Focus:</strong> PEGylation techniques and albumin-binding domains for extending pharmaceutical half-life.</p>
    </div>
  </div>
</div>

<style>
/* Timeline container */
.timeline {
  position: relative;
  max-width: 1200px;
  margin: 0 auto;
}

/* Timeline central line */
.timeline::after {
  content: '';
  position: absolute;
  width: 6px;
  background-color: #0077b6;
  top: 0;
  bottom: 0;
  left: 50%;
  margin-left: -3px;
}

/* Container for content */
.container {
  padding: 10px 40px;
  position: relative;
  background-color: inherit;
  width: 50%;
}

/* The circles on the timeline */
.container::after {
  content: '';
  position: absolute;
  width: 25px;
  height: 25px;
  right: -13px;
  background-color: white;
  border: 4px solid #0077b6;
  top: 15px;
  border-radius: 50%;
  z-index: 1;
}

/* Place the container to the left */
.left {
  left: 0;
}

/* Place the container to the right */
.right {
  left: 50%;
}

/* Add arrows to the left container */
.left::before {
  content: " ";
  height: 0;
  position: absolute;
  top: 22px;
  width: 0;
  z-index: 1;
  right: 30px;
  border: medium solid #f0f0f0;
  border-width: 10px 0 10px 10px;
  border-color: transparent transparent transparent #f0f0f0;
}

/* Add arrows to the right container */
.right::before {
  content: " ";
  height: 0;
  position: absolute;
  top: 22px;
  width: 0;
  z-index: 1;
  left: 30px;
  border: medium solid #f0f0f0;
  border-width: 10px 10px 10px 0;
  border-color: transparent #f0f0f0 transparent transparent;
}

/* Fix the circle for containers on the right side */
.right::after {
  left: -13px;
}

/* The actual content */
.content {
  padding: 20px 30px;
  background-color: #f0f0f0;
  position: relative;
  border-radius: 6px;
}

/* Date display */
.date {
  font-weight: bold;
  color: #0077b6;
  margin-bottom: 10px;
}

/* Media queries for responsiveness */
@media screen and (max-width: 600px) {
  /* Place the timelime to the left */
  .timeline::after {
    left: 31px;
  }
  
  /* Full-width containers */
  .container {
    width: 100%;
    padding-left: 70px;
    padding-right: 25px;
  }
  
  /* Make sure all circles are at the same spot */
  .left::after, .right::after {
    left: 18px;
  }
  
  /* Make all right containers behave like the left ones */
  .right {
    left: 0%;
  }
  
  /* Adjust arrows for mobile */
  .left::before, .right::before {
    left: 60px;
    border: medium solid #f0f0f0;
    border-width: 10px 10px 10px 0;
    border-color: transparent #f0f0f0 transparent transparent;
  }
}
</style>
