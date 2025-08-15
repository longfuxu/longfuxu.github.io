---
layout: about
title: welcome
permalink: /
subtitle: 

profile:
  align: right
  image: personal_pro_photo.jpg
  image_circular: false # crops the image to make it circular
  more_info: >
    <p>QB3 Institute & Department of Physics</p>
    <p>UC Berkeley/HHMI</p>
    <p>Berkeley, CA 94720, USA</p>

news: true # includes a list of news items
selected_papers: true # includes a list of papers marked as "selected={true}"
social: true # includes social icons at the bottom of the page
---

I'm a biophysicist studying viral DNA replication and packaging with single-molecule approaches. My goal is to understand how viruses replicate their genomes and package them into capsids—fundamental processes that could lead to new therapeutic targets. I'm also building **SciXchange** — a Scientific Materials Exchange Network to make research more efficient.

*Dream big, act little.*

Currently, I am a Damon Runyon Fellow and postdoctoral researcher in [Professor Carlos J. Bustamante's laboratory](http://bustamante.berkeley.edu) at UC Berkeley/HHMI. My work focuses on how ATPase motors translocate viral genomes into preassembled capsids using single-molecule biophysics techniques.

Previously, I completed my PhD and postdoctoral training in [Professor Gijs Wuite's laboratory](www.gijswuite.com) at Vrije Universiteit Amsterdam, where I developed correlative optical tweezers and fluorescence microscopy techniques. Our findings revealed that DNA replication is far more dynamic than textbooks suggest, leading to a "decentralized model" for this fundamental process (see our [Nature Communications](https://www.nature.com/articles/s41467-024-49612-3) publication).

<div class="row mt-4">
  <div class="col-md-6">
    <h3>Research Themes</h3>
    <div class="card-deck">
      <div class="card mb-3">
        <div class="card-body">
          <h5 class="card-title"><i class="fas fa-dna"></i> DNA Replication Dynamics</h5>
          <p class="card-text">Understanding how DNA polymerases exchange during replication using single-molecule approaches</p>
        </div>
      </div>
      <div class="card mb-3">
        <div class="card-body">
          <h5 class="card-title"><i class="fas fa-virus"></i> Viral Packaging</h5>
          <p class="card-text">Investigating how ATPase motors package viral genomes into capsids with force spectroscopy</p>
        </div>
      </div>
      <div class="card mb-3">
        <div class="card-body">
          <h5 class="card-title"><i class="fas fa-microscope"></i> Methodology</h5>
          <p class="card-text">Developing correlative optical tweezers and fluorescence techniques for biological studies</p>
        </div>
      </div>
    </div>
  </div>
  <div class="col-md-6">
    <h3>Latest Updates</h3>
    <div class="news">
      {% assign recent_news = site.news | sort: 'date' | reverse %}
      {% for item in recent_news limit:3 %}
        <div class="news-item">
          <div class="news-date">{{ item.date | date: "%b %Y" }}</div>
          <div class="news-content">{{ item.content | remove: '<p>' | remove: '</p>' }}</div>
        </div>
      {% endfor %}
    </div>
    
    <h3 class="mt-4">SciXchange</h3>
    <div class="alert alert-info">
      <h5 class="alert-heading">Scientific Materials Exchange Network</h5>
      <p>Building a trusted platform for researchers to share materials, reducing duplication and accelerating discovery. Currently in development.</p>
      <a href="/sciXchange/" class="btn btn-outline-primary btn-sm">Learn More</a>
    </div>
  </div>
</div>

<div class="row mt-4">
  <div class="col-12">
    <div class="text-center">
      <a href="/publications/" class="btn btn-primary me-3">View Publications</a>
      <a href="/blog/" class="btn btn-outline-secondary me-3">Read the Blog</a>
      <a href="/contact/" class="btn btn-secondary">Contact</a>
    </div>
  </div>
</div>

## research interests
- Single-molecule biophysics
- DNA-protein interactions
- Integrating structural insights with functional dynamics
- Expanding applications of single-molecule techniques
