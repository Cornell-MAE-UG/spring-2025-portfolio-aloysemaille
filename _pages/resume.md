---
layout: default
title: Resume
permalink: /resume/
---

<style>
  #english-btn, #french-btn {
    background-color: #4CAF50;
    color: white;
    padding: 10px 20px;
    border: none;
    border-radius: 5px;
    cursor: pointer;
    margin: 0 10px;
    font-size: 16px;
  }
  #english-btn:hover, #french-btn:hover {
    background-color: #45a049;
  }
  #english-btn.active, #french-btn.active {
    background-color: #45a049;
  }
</style>

<div style="text-align: center; margin-bottom: 20px; margin-top: 20px;">
  <button id="english-btn" class="active">English</button>
  <button id="french-btn">Français</button>
</div>

<div style="margin:0; padding:0;">
  <img id="english-cv" src="{{ site.baseurl }}/assets/images/CVEN.png" style="width:100%; margin:0; padding:0;" />
  <img id="french-cv" src="{{ site.baseurl }}/assets/images/CVFR.png" style="width:100%; margin:0; padding:0; display:none;" />
</div>

<script>
  const englishBtn = document.getElementById('english-btn');
  const frenchBtn = document.getElementById('french-btn');
  const englishCv = document.getElementById('english-cv');
  const frenchCv = document.getElementById('french-cv');

  englishBtn.addEventListener('click', function() {
    englishCv.style.display = 'block';
    frenchCv.style.display = 'none';
    englishBtn.classList.add('active');
    frenchBtn.classList.remove('active');
  });
  frenchBtn.addEventListener('click', function() {
    englishCv.style.display = 'none';
    frenchCv.style.display = 'block';
    frenchBtn.classList.add('active');
    englishBtn.classList.remove('active');
  });
</script>