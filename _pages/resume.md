---
layout: default
title: Resume
permalink: /resume/
---

<div style="text-align: center; margin-bottom: 20px;">
  <button id="english-btn">English</button>
  <button id="french-btn">Français</button>
</div>

<div style="margin:0; padding:0;">
  <img id="english-cv" src="{{ site.baseurl }}/assets/images/CVEN.png" style="width:100%; margin:0; padding:0;" />
  <img id="french-cv" src="{{ site.baseurl }}/assets/images/CVFR.png" style="width:100%; margin:0; padding:0; display:none;" />
</div>

<script>
  document.getElementById('english-btn').addEventListener('click', function() {
    document.getElementById('english-cv').style.display = 'block';
    document.getElementById('french-cv').style.display = 'none';
  });
  document.getElementById('french-btn').addEventListener('click', function() {
    document.getElementById('english-cv').style.display = 'none';
    document.getElementById('french-cv').style.display = 'block';
  });
</script>