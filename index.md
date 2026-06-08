---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: page
title: Home
# page_title intentionally omitted — the hero below carries the title.
---

<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&family=Lora:ital,wght@0,500;0,600;1,500&display=swap" rel="stylesheet">

<style>
/* ===== Design tokens ===== */
:root {
  --navy: #0a3161;       /* CWRU navy */
  --navy-deep: #061428;
  --blue: #1d6fb8;
  --accent: #c8102e;     /* CWRU-ish accent red, used sparingly */
  --ink: #1f2733;
  --muted: #5b6675;
  --line: #e6e9ee;
  --card-shadow: 0 6px 22px rgba(10, 49, 97, 0.10);
  --card-shadow-hover: 0 14px 34px rgba(10, 49, 97, 0.18);
}

/* ===== Homepage scope ===== */
.home {
  font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', Helvetica, Arial, sans-serif;
  color: var(--ink);
  -webkit-font-smoothing: antialiased;
}
.home a { color: var(--blue); text-decoration: none; }
.home a:hover { text-decoration: underline; }

/* entrance animation */
@keyframes riseIn { from { opacity: 0; transform: translateY(16px); } to { opacity: 1; transform: none; } }
.home .reveal { animation: riseIn 0.7s ease both; }
.home .reveal.d1 { animation-delay: 0.08s; }
.home .reveal.d2 { animation-delay: 0.16s; }
.home .reveal.d3 { animation-delay: 0.24s; }

/* ===== Hero / slideshow ===== */
.home-hero {
  position: relative;
  width: 100%;
  margin: 0 0 26px;
}
.slideshow {
  position: relative;
  width: 100%;
  aspect-ratio: 16 / 7;
  overflow: hidden;
  border-radius: 16px;
  box-shadow: 0 18px 48px rgba(6, 20, 40, 0.28);
  background: #000;
}
.slideshow .slide {
  position: absolute; inset: 0;
  width: 100%; height: 100%;
  object-fit: cover;
  opacity: 0;
  transform: scale(1.06);
  transition: opacity 1.1s ease-in-out, transform 6s ease-out;
}
.slideshow .slide.active { opacity: 1; transform: scale(1); }

/* gradient scrim + title overlay */
.hero-overlay {
  position: absolute; inset: 0;
  display: flex; flex-direction: column; justify-content: flex-end;
  padding: 6% 70px 6%;
  background: linear-gradient(to top, rgba(6,20,40,0.84) 0%, rgba(6,20,40,0.38) 40%, rgba(6,20,40,0.05) 66%, rgba(6,20,40,0) 100%);
  pointer-events: none;
}
.hero-eyebrow {
  display: inline-block;
  font-size: clamp(0.7rem, 1.1vw, 0.82rem);
  letter-spacing: 0.22em;
  text-transform: uppercase;
  font-weight: 600;
  color: #bcd4ef;
  margin-bottom: 10px;
}
.hero-title {
  margin: 0;
  color: #fff;
  font-family: 'Lora', Georgia, serif;
  font-weight: 600;
  font-size: clamp(1.3rem, 2.1vw, 2.05rem);
  line-height: 1.14;
  text-shadow: 0 2px 18px rgba(0,0,0,0.45);
  max-width: 20ch;
}
.hero-title .uni { color: #ffd86b; }
.hero-rule {
  width: 64px; height: 4px; margin-top: 18px;
  background: linear-gradient(90deg, #ffd86b, var(--accent));
  border-radius: 4px;
}

/* arrows */
.slideshow .nav-arrow {
  position: absolute; top: 50%; transform: translateY(-50%);
  display: flex; align-items: center; justify-content: center;
  width: 44px; height: 44px;
  background: rgba(255,255,255,0.16);
  backdrop-filter: blur(4px);
  color: #fff; border: 1px solid rgba(255,255,255,0.35);
  font-size: 1.3rem; cursor: pointer; user-select: none;
  border-radius: 50%; transition: background 0.2s, transform 0.2s;
  z-index: 3;
}
.slideshow .nav-arrow:hover { background: rgba(255,255,255,0.34); }
.slideshow .nav-prev { left: 16px; }
.slideshow .nav-next { right: 16px; }

/* dots */
.slideshow .dots {
  position: absolute; bottom: 16px; right: 22px; left: auto;
  text-align: right; z-index: 3;
}
.slideshow .dot {
  display: inline-block; width: 9px; height: 9px; margin: 0 4px;
  border-radius: 50%; background: rgba(255,255,255,0.45);
  cursor: pointer; transition: background 0.25s, transform 0.25s;
}
.slideshow .dot.active { background: #ffd86b; transform: scale(1.3); }

/* ===== Two-column body ===== */
.home-body { display: flex; gap: 40px; align-items: flex-start; }
.home-main { flex: 2 1 0; min-width: 0; }
.home-aside { flex: 1 1 0; min-width: 0; }

/* section heading */
.section-eyebrow {
  display: block;
  font-size: 0.74rem; letter-spacing: 0.2em; text-transform: uppercase;
  font-weight: 700; color: var(--blue); margin-bottom: 4px;
}
.section-title {
  margin: 0 0 18px;
  font-family: 'Lora', Georgia, serif;
  font-weight: 600; font-size: 1.7rem; color: var(--navy);
  position: relative; padding-bottom: 12px;
}
.section-title::after {
  content: ""; position: absolute; left: 0; bottom: 0;
  width: 54px; height: 3px; border-radius: 3px;
  background: linear-gradient(90deg, var(--navy), var(--blue));
}

.lede {
  font-size: 1.08rem; line-height: 1.75; color: var(--ink);
  text-align: justify;
}
.cta-banner {
  margin-top: 24px; padding: 18px 22px;
  background: linear-gradient(135deg, rgba(29,111,184,0.08), rgba(10,49,97,0.06));
  border-left: 4px solid var(--blue);
  border-radius: 10px; font-size: 1rem; line-height: 1.6;
}

/* news paged carousel (rotates like the hero slideshow) */
.news-carousel {
  position: relative;
  transition: height 0.4s ease;
}
.news-slide {
  position: absolute; top: 0; left: 0; right: 0;
  opacity: 0; visibility: hidden;
  transform: translateY(10px);
  transition: opacity 0.7s ease, transform 0.7s ease, visibility 0.7s;
}
.news-slide.active {
  opacity: 1; visibility: visible; transform: none;
  position: relative;
}
.news-slide .news-card { margin-bottom: 14px; }
.news-slide .news-card:last-child { margin-bottom: 0; }

.news-dots { text-align: center; margin-top: 14px; }
.news-dots .ndot {
  display: inline-block; width: 9px; height: 9px; margin: 0 5px;
  border-radius: 50%; background: #c7d2e0; cursor: pointer;
  transition: background 0.25s, transform 0.25s;
}
.news-dots .ndot.active { background: var(--navy); transform: scale(1.3); }

/* news cards */
.news-list { list-style: none; padding: 0; margin: 0; }
.news-card {
  position: relative;
  padding: 16px 18px; margin-bottom: 14px;
  background: #fff; border: 1px solid var(--line);
  border-radius: 12px; box-shadow: var(--card-shadow);
  transition: transform 0.2s ease, box-shadow 0.2s ease;
}
.news-card:hover { transform: translateY(-3px); box-shadow: var(--card-shadow-hover); }
.news-date {
  display: inline-block; font-size: 0.72rem; font-weight: 700;
  letter-spacing: 0.06em; text-transform: uppercase;
  color: #fff; background: var(--navy);
  padding: 3px 9px; border-radius: 999px; margin-bottom: 8px;
}
.news-text { font-size: 0.95rem; line-height: 1.5; color: var(--ink); display: block; }
.news-more {
  display: inline-flex; align-items: center; gap: 6px;
  margin-top: 6px; font-weight: 600; font-size: 0.95rem;
}
.news-more::after { content: "→"; transition: transform 0.2s; }
.news-more:hover { text-decoration: none; }
.news-more:hover::after { transform: translateX(4px); }

/* ===== Funding ===== */
.funding {
  margin-top: 56px; padding: 38px 24px 30px;
  background: linear-gradient(180deg, #f7f9fc, #eef2f8);
  border-radius: 18px; text-align: center;
}
.funding .section-eyebrow { color: var(--navy); }
.funding .section-title { display: inline-block; }
.funding .section-title::after { left: 50%; transform: translateX(-50%); }
.funding-logos {
  display: flex; flex-wrap: wrap; justify-content: center; align-items: center;
  gap: 20px; margin-top: 26px;
}
.funder {
  display: flex; align-items: center; justify-content: center;
  height: 104px; width: 188px; padding: 16px 22px;
  background: #fff; border: 1px solid var(--line);
  border-radius: 14px; box-shadow: var(--card-shadow);
  transition: transform 0.2s ease, box-shadow 0.2s ease;
}
.funder:hover { transform: translateY(-3px); box-shadow: var(--card-shadow-hover); }
.funder img {
  max-height: 100%; max-width: 100%; width: auto; object-fit: contain;
  filter: grayscale(100%); opacity: 0.78;
  transition: filter 0.25s ease, opacity 0.25s ease;
}
.funder:hover img { filter: grayscale(0%); opacity: 1; }
.funding-logos .placeholder {
  display: flex; align-items: center; justify-content: center;
  height: 104px; min-width: 188px; padding: 0 18px;
  background: #fff; border: 1px dashed #b0b0b0;
  border-radius: 14px; color: var(--muted); font-size: 0.9rem; font-weight: 500;
}

/* ===== Responsive ===== */
@media (max-width: 820px) {
  .home-body { flex-direction: column; gap: 30px; }
  .slideshow { aspect-ratio: 4 / 3; border-radius: 12px; }
  .hero-title { max-width: 100%; }
}
</style>

<div class="home">

<!-- ============ TWO-COLUMN BODY ============ -->
<div class="home-body">

  <!-- LEFT: Hero slideshow + Who we are -->
  <div class="home-main reveal d1">

    <!-- HERO SLIDESHOW (column width) -->
    <div class="home-hero">
      <div class="slideshow" id="labSlideshow">
        <!-- SLIDES:START — auto-listed from /pics/slideshow/. Just drop images in that folder. -->
        {% assign slide_files = site.static_files | where_exp: "f", "f.path contains '/pics/slideshow/'" | sort: "path" %}
        {% for f in slide_files %}{% assign ext = f.extname | downcase %}{% if ext == ".jpg" or ext == ".jpeg" or ext == ".png" or ext == ".webp" %}<img class="slide{% if forloop.first %} active{% endif %}" src="{{ f.path | relative_url }}" alt="Lab photo {{ forloop.index }}">
        {% endif %}{% endfor %}
        <!-- SLIDES:END -->

        <div class="hero-overlay">
          <span class="hero-eyebrow">Cancer Epigenomics</span>
          <h1 class="hero-title">Welcome to the Gao Lab <span class="uni">@ Case Western Reserve University</span></h1>
          <div class="hero-rule"></div>
        </div>

        <button class="nav-arrow nav-prev" onclick="changeSlide(-1)" aria-label="Previous slide">&#10094;</button>
        <button class="nav-arrow nav-next" onclick="changeSlide(1)" aria-label="Next slide">&#10095;</button>

        <div class="dots" id="slideshowDots"></div>
      </div>
    </div>

    <span class="section-eyebrow">About the Lab</span>
    <h2 class="section-title">Who We Are</h2>
    <p class="lede">
    We are a cancer epigenomics lab based in the <a href="https://case.edu/medicine/pharmacology/">Department of Pharmacology</a> at Case Western Reserve University, School of Medicine. Our research is dedicated to uncovering novel fundamental mechanisms underlying gene expression in cancers. We utilize advanced multi-omics technologies, including high-throughput CRISPR screening, single-cell transcriptomics, epigenomics, proteomics, and metabolomics to comprehensively detail the oncogenic mechanisms of transcription factors and identify therapeutic targets for treatment.
    </p>
    <div class="cta-banner">
      <strong>We are currently seeking postdocs, students, and staff to join our team.</strong> For more information, please view our available <a href="https://ygaoyg.github.io/join/">opportunities</a>.
    </div>
  </div>

  <!-- RIGHT: News -->
  <aside class="home-aside reveal d2">
    <span class="section-eyebrow">Updates</span>
    <h2 class="section-title">Lab News</h2>
    <div class="news-carousel" id="newsCarousel">
      <!-- Add more <div class="news-card">…</div> blocks below (newest first).
           They auto-group into pages of two. -->
      <div class="news-source" id="newsSource">
        <!-- NEWS:START — auto-generated from _data/news.yml (newest first) -->
        {% assign news_items = site.data.news | sort: "date" | reverse %}
        {% for item in news_items %}
        <div class="news-card">
          <span class="news-date">{{ item.date_display }}</span>
          <span class="news-text">{{ item.text }}</span>
        </div>
        {% endfor %}
        <!-- NEWS:END -->
      </div>
    </div>
    <div class="news-dots" id="newsDots"></div>
    <a class="news-more" href="https://ygaoyg.github.io/news/">More news</a>
  </aside>

</div>

<!-- ============ FUNDING ============ -->
<div class="funding reveal d3">
  <span class="section-eyebrow">Support</span>
  <h2 class="section-title">Funding &amp; Support</h2>
  <div class="funding-logos">
    <div class="funder"><img src="pics/logo-nci.svg" alt="National Cancer Institute"></div>
    <div class="funder"><img src="pics/logo-bplus.jpg" alt="Andrew McDonough B+ Foundation"></div>
    <div class="funder"><img src="pics/logo-charlie-landers.svg" alt="Charlie Landers Foundation"></div>
    <div class="funder"><img src="pics/logo-rally.jpg" alt="Rally Foundation for Childhood Cancer Research"></div>
    <div class="funder"><img src="pics/logo-velosano.webp" alt="VeloSano"></div>
  </div>
</div>

</div><!-- /.home -->

<!-- ============ SLIDESHOW SCRIPT ============ -->
<script>
(function () {
  var slideshow = document.getElementById('labSlideshow');
  if (!slideshow) return;
  var slides = slideshow.querySelectorAll('.slide');
  var dotsContainer = document.getElementById('slideshowDots');
  var current = 0;
  var timer = null;
  var INTERVAL = 5000;

  slides.forEach(function (s, i) {
    var dot = document.createElement('span');
    dot.className = 'dot' + (i === 0 ? ' active' : '');
    dot.addEventListener('click', function () { goTo(i); });
    dotsContainer.appendChild(dot);
  });
  var dots = dotsContainer.querySelectorAll('.dot');

  function render() {
    slides.forEach(function (s, i) { s.classList.toggle('active', i === current); });
    dots.forEach(function (d, i) { d.classList.toggle('active', i === current); });
  }
  function goTo(i) {
    current = (i + slides.length) % slides.length;
    render();
    restart();
  }
  window.changeSlide = function (dir) { goTo(current + dir); };

  function restart() {
    if (timer) clearInterval(timer);
    timer = setInterval(function () { goTo(current + 1); }, INTERVAL);
  }
  render();
  restart();
})();

/* ===== Lab News paged carousel (rotates like the hero) ===== */
(function () {
  var carousel = document.getElementById('newsCarousel');
  var dotsContainer = document.getElementById('newsDots');
  if (!carousel || !dotsContainer) return;

  var PER_PAGE = 4; // how many news items to show per page

  // collect the source cards, then group them into pages
  var source = document.getElementById('newsSource');
  var cards = source ? Array.prototype.slice.call(source.querySelectorAll('.news-card')) : [];
  if (cards.length === 0) return;

  carousel.innerHTML = '';
  for (var i = 0; i < cards.length; i += PER_PAGE) {
    var slide = document.createElement('div');
    slide.className = 'news-slide' + (i === 0 ? ' active' : '');
    for (var j = i; j < Math.min(i + PER_PAGE, cards.length); j++) {
      slide.appendChild(cards[j]);
    }
    carousel.appendChild(slide);
  }
  var slides = carousel.querySelectorAll('.news-slide');

  var current = 0;
  var timer = null;
  var INTERVAL = 5000;

  // build dots (hidden when there is only one page)
  if (slides.length <= 1) { dotsContainer.style.display = 'none'; }
  slides.forEach(function (s, i) {
    var dot = document.createElement('span');
    dot.className = 'ndot' + (i === 0 ? ' active' : '');
    dot.addEventListener('click', function () { go(i); });
    dotsContainer.appendChild(dot);
  });
  var dots = dotsContainer.querySelectorAll('.ndot');

  // lock the height to the tallest slide so cards don't jump while fading
  function sizeIt() {
    var h = 0;
    slides.forEach(function (s) { h = Math.max(h, s.offsetHeight); });
    if (h > 0) carousel.style.height = h + 'px';
  }

  function render() {
    slides.forEach(function (s, i) { s.classList.toggle('active', i === current); });
    dots.forEach(function (d, i) { d.classList.toggle('active', i === current); });
  }
  function go(i) {
    current = (i + slides.length) % slides.length;
    render();
    restart();
  }
  function restart() {
    if (timer) clearInterval(timer);
    if (slides.length > 1) timer = setInterval(function () { go(current + 1); }, INTERVAL);
  }

  // pause on hover
  carousel.addEventListener('mouseenter', function () { if (timer) clearInterval(timer); });
  carousel.addEventListener('mouseleave', restart);

  function start() { sizeIt(); render(); restart(); }
  if (document.readyState === 'complete') { start(); }
  else { window.addEventListener('load', start); }
  window.addEventListener('resize', sizeIt);
})();
</script>
