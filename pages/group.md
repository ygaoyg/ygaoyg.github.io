---
layout: page
title: Group
page_title: Group
permalink: /group/
---

<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&family=Lora:wght@500;600&display=swap" rel="stylesheet">

<style>
.group { font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', Helvetica, Arial, sans-serif; color: #1f2733; }
.group a { color: #1d6fb8; text-decoration: none; }
.group a:hover { text-decoration: underline; }

.group-section {
  font-family: 'Lora', Georgia, serif;
  font-weight: 600; font-size: 1.5rem; color: #0a3161;
  margin: 38px 0 22px; padding-bottom: 10px; position: relative;
}
.group-section::after {
  content: ""; position: absolute; left: 0; bottom: 0;
  width: 52px; height: 3px; border-radius: 3px;
  background: linear-gradient(90deg, #0a3161, #1d6fb8);
}

.member {
  display: flex; align-items: flex-start; gap: 26px;
  margin-bottom: 30px;
}
.member-photo {
  flex: 0 0 auto;
  width: 168px; height: 168px;
  object-fit: cover; object-position: center top;
  border-radius: 16px;
  box-shadow: 0 8px 22px rgba(10, 49, 97, 0.16);
}
.member-body { flex: 1 1 0; min-width: 0; }
.member-name {
  font-family: 'Lora', Georgia, serif;
  font-weight: 600; font-size: 1.3rem; color: #0a3161;
  margin: 2px 0 2px;
}
.member-role {
  font-size: 0.74rem; font-weight: 700; letter-spacing: 0.12em;
  text-transform: uppercase; color: #1d6fb8; margin-bottom: 10px;
}
.member-bio { text-align: justify; line-height: 1.6; margin: 0; }

/* Alumni table */
.alumni-table { width: 100%; border-collapse: collapse; margin-top: 6px; }
.alumni-table th, .alumni-table td {
  text-align: left; padding: 10px 12px; border-bottom: 1px solid #e6e9ee; font-size: 0.95rem;
}
.alumni-table th {
  font-size: 0.74rem; letter-spacing: 0.08em; text-transform: uppercase;
  color: #0a3161; border-bottom: 2px solid #0a3161;
}

@media (max-width: 600px) {
  .member { gap: 18px; }
  .member-photo { width: 110px; height: 110px; border-radius: 12px; }
}
</style>

<div class="group">

<h2 class="group-section">Principal Investigator</h2>

<div class="member">
  <img class="member-photo" src="../pics/yuan-gao-new.jpg" alt="Yuan Gao">
  <div class="member-body">
    <div class="member-name">Yuan Gao, PhD</div>
    <div class="member-role">Assistant Professor</div>
    <p class="member-bio">Dr. Yuan Gao is an Assistant Professor in the Department of Pharmacology at Case Western Reserve University, School of Medicine, where she established her lab in 2024. She earned her Ph.D. in Biochemistry and Molecular Biology from Mayo Clinic College of Medicine and completed her postdoctoral training in Dr. Christopher Vakoc's lab at Cold Spring Harbor Laboratory.</p>
  </div>
</div>

<h2 class="group-section">Postdoctoral Fellows</h2>

<div class="member">
  <img class="member-photo" src="../pics/hang-zhao.jpg" alt="Hang Zhao">
  <div class="member-body">
    <div class="member-name">Hang Zhao, PhD</div>
    <div class="member-role">Postdoctoral Fellow</div>
    <p class="member-bio">Dr. Hang Zhao earned a Ph.D. in Biochemistry and Molecular Biology from the School of Life Sciences at Peking University, advised by Dr. Qing Li, after completing a B.Sc. in Biological Science at Xiamen University under Dr. Jiahuai Han. Hang joined the Gao Lab as a postdoctoral fellow.</p>
  </div>
</div>

<h2 class="group-section">Graduate Students</h2>

<div class="member">
  <img class="member-photo" src="../pics/muyi-ye.jpg" alt="Muyi (Felix) Ye">
  <div class="member-body">
    <div class="member-name">Muyi (Felix) Ye</div>
    <div class="member-role">Graduate Student</div>
    <p class="member-bio">Muyi (Felix) Ye is a graduate student in the Department of Pharmacology. He earned his Bachelor's degree in Biochemistry from Case Western Reserve University in 2024.</p>
  </div>
</div>

<div class="member">
  <img class="member-photo" src="../pics/yeriel.jpg" alt="Yeriel Avellanet-Crespo">
  <div class="member-body">
    <div class="member-name">Yeriel Avellanet-Crespo</div>
    <div class="member-role">Graduate Student</div>
    <p class="member-bio">Yeriel is a graduate student in the Department of Genetics and Genome Sciences. He earned his Bachelor's degree in Chemistry and Molecular Cell Biology from the University of Puerto Rico in 2024.</p>
  </div>
</div>

<h2 class="group-section">Research Assistants</h2>

<div class="member">
  <img class="member-photo" src="../pics/anton-new.jpg" alt="Anton Sergeev">
  <div class="member-body">
    <div class="member-name">Anton Sergeev</div>
    <div class="member-role">Research Assistant</div>
    <p class="member-bio">Anton works as a research assistant in the lab. He obtained his bachelor's degree from Boston University in 2024.</p>
  </div>
</div>

<h2 class="group-section">Alumni</h2>

<table class="alumni-table">
  <thead>
    <tr><th>Name</th><th>Role</th></tr>
  </thead>
  <tbody>
    <tr><td>Alvin Liu</td><td>Research Assistant</td></tr>
    <tr><td>Saanvi Srivastava</td><td>Undergraduate Research Assistant</td></tr>
    <tr><td>Joy Fei</td><td>Undergraduate Research Assistant</td></tr>
  </tbody>
</table>

</div>
