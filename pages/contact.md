---
layout: page
title: Contact
page_title: Contact
permalink: /contact/
---

<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&family=Lora:wght@500;600&display=swap" rel="stylesheet">

<style>
.contact { font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', Helvetica, Arial, sans-serif; color: #1f2733; }
.contact a { color: #1d6fb8; text-decoration: none; }
.contact a:hover { text-decoration: underline; }

.contact-card {
  display: flex; gap: 28px; align-items: flex-start;
  background: #fff; border: 1px solid #e6e9ee; border-radius: 18px;
  box-shadow: 0 10px 28px rgba(10, 49, 97, 0.10);
  padding: 28px; max-width: 720px;
}
.contact-photo {
  flex: 0 0 auto; width: 140px; height: 140px;
  object-fit: cover; object-position: center top; border-radius: 14px;
  box-shadow: 0 6px 16px rgba(10, 49, 97, 0.16);
}
.contact-name { font-family: 'Lora', Georgia, serif; font-size: 1.5rem; color: #0a3161; margin: 2px 0 4px; }
.contact-title {
  font-size: 0.76rem; font-weight: 700; letter-spacing: 0.08em; text-transform: uppercase;
  color: #1d6fb8; margin-bottom: 18px;
}
.contact-row { display: flex; align-items: flex-start; gap: 12px; margin-bottom: 12px; font-size: 1rem; line-height: 1.45; }
.contact-row .ico { flex: 0 0 auto; width: 22px; text-align: center; font-size: 1rem; }
.contact-label {
  display: block; font-size: 0.7rem; font-weight: 700; letter-spacing: 0.06em;
  text-transform: uppercase; color: #0a3161; margin-bottom: 1px;
}

@media (max-width: 560px) {
  .contact-card { flex-direction: column; align-items: center; text-align: center; }
  .contact-row { text-align: left; }
}
</style>

<div class="contact">

<div class="contact-card">
  <img class="contact-photo" src="../pics/yuan-gao-new.jpg" alt="Yuan Gao">
  <div class="contact-body">
    <h2 class="contact-name">Yuan Gao, PhD</h2>
    <div class="contact-title">Principal Investigator &middot; Department of Pharmacology, CWRU</div>

    <div class="contact-row">
      <span class="ico">&#9993;</span>
      <div><span class="contact-label">Email</span><a href="mailto:yxg811@case.edu">yxg811@case.edu</a></div>
    </div>
    <div class="contact-row">
      <span class="ico">&#9742;</span>
      <div><span class="contact-label">Office</span>(216) 368-6632</div>
    </div>
    <div class="contact-row">
      <span class="ico">&#128205;</span>
      <div><span class="contact-label">Address</span>
        <a href="https://maps.google.com/?q=2109+Adelbert+Rd,+Cleveland,+OH+44106" target="_blank">2109 Adelbert Rd, RT300-7, Cleveland, OH 44106</a>
      </div>
    </div>
  </div>
</div>

</div>
