---
layout: page
title: News
page_title: News
permalink: /news/
---

<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&family=Lora:wght@500;600&display=swap" rel="stylesheet">

<style>
.news-page { font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', Helvetica, Arial, sans-serif; color: #1f2733; }
.news-intro { color: #5b6675; font-size: 1rem; margin: 0 0 26px; }

.news-feed { position: relative; }
.news-entry {
  display: flex; gap: 26px; align-items: flex-start;
  background: #fff; border: 1px solid #e6e9ee; border-radius: 16px;
  box-shadow: 0 8px 22px rgba(10, 49, 97, 0.08);
  padding: 18px; margin-bottom: 26px;
  transition: box-shadow 0.2s ease, transform 0.2s ease;
}
.news-entry:hover { box-shadow: 0 14px 32px rgba(10, 49, 97, 0.15); transform: translateY(-2px); }
.news-entry-photo {
  flex: 0 0 auto; width: 320px; max-width: 42%;
  aspect-ratio: 4 / 3; object-fit: cover; border-radius: 12px;
}
.news-entry-photo.is-logo {
  object-fit: contain; background: #fff;
  padding: 18px; border: 1px solid #e6e9ee;
}
.news-entry-body { flex: 1 1 0; min-width: 0; }
.news-entry-date {
  display: inline-block; font-size: 0.74rem; font-weight: 700;
  letter-spacing: 0.06em; text-transform: uppercase; color: #fff;
  background: #0a3161; padding: 4px 11px; border-radius: 999px; margin-bottom: 12px;
}
.news-entry-text { font-size: 1.02rem; line-height: 1.6; margin: 0; }

@media (max-width: 700px) {
  .news-entry { flex-direction: column; gap: 16px; }
  .news-entry-photo { width: 100%; max-width: 100%; }
}
</style>

<div class="news-page">

<p class="news-intro">Moments from life in the Gao Lab &mdash; celebrations, milestones, and new faces.</p>

<div class="news-feed">
<!-- NEWSPAGE:START — auto-generated from _data/news.yml (newest first) -->
{% assign news_items = site.data.news | sort: "date" | reverse %}
{% for item in news_items %}
<article class="news-entry">
  {% if item.photo %}<img class="news-entry-photo{% if item.logo %} is-logo{% endif %}" src="../pics/{{ item.photo }}" alt="Lab news photo">{% endif %}
  <div class="news-entry-body">
    <span class="news-entry-date">{{ item.date_display }}</span>
    <p class="news-entry-text">{{ item.text }}</p>
  </div>
</article>
{% endfor %}
<!-- NEWSPAGE:END -->
</div>

</div>
