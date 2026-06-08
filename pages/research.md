---
layout: page
title: Research
page_title: Research
permalink: /research/
---

<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&family=Lora:ital,wght@0,500;0,600;1,500&display=swap" rel="stylesheet">

<style>
.research { font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', Helvetica, Arial, sans-serif; color: #1f2733; }
.research a { color: #1d6fb8; text-decoration: none; }
.research a:hover { text-decoration: underline; }

.research-lede { font-size: 1.14rem; line-height: 1.75; max-width: 840px; text-align: justify; }
.research-lede strong { color: #0a3161; }
.research-lede .pull {
  display: block; margin: 22px auto 8px; max-width: 720px;
  font-family: 'Lora', Georgia, serif; font-style: italic;
  font-size: 1.25rem; line-height: 1.4; color: #0a3161; text-align: center;
}

.directions-title {
  font-family: 'Lora', Georgia, serif; font-weight: 600; font-size: 1.5rem; color: #0a3161;
  margin: 38px 0 22px; padding-bottom: 10px; position: relative;
}
.directions-title::after {
  content: ""; position: absolute; left: 0; bottom: 0;
  width: 52px; height: 3px; border-radius: 3px;
  background: linear-gradient(90deg, #0a3161, #1d6fb8);
}

.direction {
  display: flex; gap: 24px; align-items: flex-start;
  background: #fff; border: 1px solid #e6e9ee; border-radius: 16px;
  box-shadow: 0 8px 22px rgba(10, 49, 97, 0.08);
  padding: 24px; margin-bottom: 20px;
  transition: transform 0.2s ease, box-shadow 0.2s ease;
}
.direction:hover { transform: translateY(-3px); box-shadow: 0 14px 32px rgba(10, 49, 97, 0.15); }
.direction-num {
  flex: 0 0 auto; width: 54px; height: 54px; border-radius: 14px;
  display: flex; align-items: center; justify-content: center;
  font-family: 'Lora', Georgia, serif; font-weight: 600; font-size: 1.5rem; color: #fff;
  background: linear-gradient(135deg, #0a3161, #1d6fb8);
}
.direction-body h3 { font-family: 'Lora', Georgia, serif; color: #0a3161; font-size: 1.22rem; margin: 6px 0 8px; }
.direction-body p { margin: 0; line-height: 1.6; color: #3a4452; }

@media (max-width: 600px) {
  .direction { gap: 16px; padding: 18px; }
  .direction-num { width: 44px; height: 44px; font-size: 1.2rem; }
}
</style>

<div class="research">

<p class="research-lede">
Our lab studies <strong>cancer-specific transcription factor (TF) dependencies</strong>, the master regulators of gene expression that tumors become addicted to, yet normal cells can live without. These transcription factors have long been considered &ldquo;undruggable,&rdquo; and we develop new strategies to target them, turning a cancer&rsquo;s reliance on a TF into a therapeutic vulnerability and, ultimately, <strong>better treatments</strong>. We use Ewing sarcoma, where we discovered the essential TF ETV6, as a flagship model, and extend these approaches to other TF-driven cancers.
<span class="pull">Every cancer-specific dependency is a therapeutic opportunity.</span>
We pursue this through three complementary directions:
</p>

<h2 class="directions-title">Research Directions</h2>

<div class="direction">
  <div class="direction-num">1</div>
  <div class="direction-body">
    <h3>Targeting essential protein interactions of TF dependencies</h3>
    <p>Cancer-dependent transcription factors act through interactions with partner proteins. We map these interactions and pinpoint the ones tumor cells cannot live without, then disrupt them as a therapeutic strategy.</p>
  </div>
</div>

<div class="direction">
  <div class="direction-num">2</div>
  <div class="direction-body">
    <h3>Ligand modulation of transcription factors</h3>
    <p>Transcription factors have long been considered difficult to drug. We are exploring how small molecules and metabolites can bind and modulate these factors, aiming to pharmacologically tune their activity and unlock new therapeutic targets.</p>
  </div>
</div>

<div class="direction">
  <div class="direction-num">3</div>
  <div class="direction-body">
    <h3>Modeling the tumor microenvironment to identify acquired dependencies</h3>
    <p>Using custom microfluidic &ldquo;sarcoma-on-a-chip&rdquo; devices, we reconstruct the tumor microenvironment to uncover the acquired dependencies and resistance mechanisms it creates, and reveal new vulnerabilities to target therapeutically.</p>
  </div>
</div>

</div>
