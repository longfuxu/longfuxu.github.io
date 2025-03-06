---
layout: page
permalink: /publications/
title: publications
description: Research publications in biophysics and molecular mechanisms, including work in Nature Communications and Nucleic Acids Research.
nav: true
nav_order: 4
---

<!-- _pages/publications.md -->

<div class="publication-metrics">
  <h2>Publication Impact</h2>
  <div class="metrics-container">
    <div class="metric-card">
      <div class="metric-value">6</div>
      <div class="metric-label">Publications</div>
    </div>
    <div class="metric-card">
      <div class="metric-value">50+</div>
      <div class="metric-label">Citations</div>
    </div>
    <div class="metric-card">
      <div class="metric-value">3</div>
      <div class="metric-label">High-Impact Journals</div>
    </div>
  </div>
  
  <div class="journal-impact">
    <h3>Journal Highlights</h3>
    <ul>
      <li><strong>Nature Communications</strong> - Impact Factor: 16.6</li>
      <li><strong>Nucleic Acids Research</strong> - Impact Factor: 16.9</li>
      <li><strong>International Journal of Molecular Sciences</strong> - Impact Factor: 5.6</li>
    </ul>
  </div>
  
  <div class="research-highlights">
    <h3>Research Highlights</h3>
    <div class="highlight-item">
      <h4>Decentralized Model of DNA Replication</h4>
      <p>Our work on DNA polymerase exchange during replication has challenged the traditional model of replication dynamics, proposing a more dynamic and decentralized process. This finding has significant implications for understanding DNA replication mechanisms and potential applications in biotechnology.</p>
      <p><em>Published in Nature Communications (2024)</em></p>
    </div>
    <div class="highlight-item">
      <h4>T7 Gp2.5 Binding Dynamics</h4>
      <p>Our research on the regulation of T7 Gp2.5 binding dynamics by its C-terminal tail has provided new insights into how single-stranded DNA binding proteins coordinate DNA metabolism, with implications for understanding DNA replication, recombination, and repair.</p>
      <p><em>Published in Nucleic Acids Research (2023)</em></p>
    </div>
  </div>
</div>

<style>
.publication-metrics {
  margin-bottom: 40px;
}

.metrics-container {
  display: flex;
  justify-content: space-between;
  margin: 30px 0;
  flex-wrap: wrap;
}

.metric-card {
  background-color: #f8f9fa;
  border-radius: 8px;
  padding: 20px;
  text-align: center;
  width: 30%;
  box-shadow: 0 4px 6px rgba(0,0,0,0.1);
  transition: transform 0.3s ease;
}

.metric-card:hover {
  transform: translateY(-5px);
}

.metric-value {
  font-size: 2.5rem;
  font-weight: bold;
  color: #0077b6;
  margin-bottom: 10px;
}

.metric-label {
  font-size: 1rem;
  color: #555;
}

.journal-impact, .research-highlights {
  margin-top: 40px;
}

.highlight-item {
  margin-bottom: 25px;
  padding-bottom: 25px;
  border-bottom: 1px solid #eee;
}

.highlight-item:last-child {
  border-bottom: none;
}

.highlight-item h4 {
  color: #333;
  margin-bottom: 10px;
}

@media (max-width: 768px) {
  .metrics-container {
    flex-direction: column;
  }
  
  .metric-card {
    width: 100%;
    margin-bottom: 15px;
  }
}
</style>

<!-- Bibsearch Feature -->

{% include bib_search.liquid %}

<div class="publications">

{% bibliography %}

</div>
