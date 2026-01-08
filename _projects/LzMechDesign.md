---
layout: project
title: WINDSTOP
description: Intro to mech design project
technologies: [sketching, CAD, testing, design process]
image: /assets/images/IMD0.png
---

<div class="carousel">
  <div class="carousel-container">
    <div class="left"><img id="left-img" src="" /></div>
    <div class="center"><img id="center-img" src="" /></div>
    <div class="right"><img id="right-img" src="" /></div>
  </div>
  <button class="carousel-btn prev" onclick="prevSlide()">&#10094;</button>
  <button class="carousel-btn next" onclick="nextSlide()">&#10095;</button>
</div>

<div class="technologies">
  {% for tech in page.technologies %}
    <span class="tech-box">{{ tech }}</span>
  {% endfor %}
</div>

<script>
  const images = [
    '{{ site.baseurl }}/assets/images/IMD1.JPEG',
    '{{ site.baseurl }}/assets/images/IMD2.JPEG',
    '{{ site.baseurl }}/assets/images/IMD3.png'
  ];
  let currentIndex = 0;

  function updateCarousel() {
    const leftIndex = (currentIndex - 1 + images.length) % images.length;
    const rightIndex = (currentIndex + 1) % images.length;
    document.getElementById('left-img').src = images[leftIndex];
    document.getElementById('center-img').src = images[currentIndex];
    document.getElementById('right-img').src = images[rightIndex];
  }

  function nextSlide() {
    currentIndex = (currentIndex + 1) % images.length;
    updateCarousel();
  }

  function prevSlide() {
    currentIndex = (currentIndex - 1 + images.length) % images.length;
    updateCarousel();
  }

  // Initialize
  updateCarousel();
</script>


<div>
<p>This project was part of my Intro to Mechanical Design class of Spring 2025.</p>
    
<p>My team decided to create an easy adaptable device to fix to any window and fix its opening to a set point, even in cases of strong winds. The devices has for main target audience students or people leasing their place of living, who cannot install permanent devices on their window and rely primarly on the use of their windows to regulate the temperature of their households.</p>

<p>Several prototypes of the design were made using mainly laser cutting and 3D printing, and the industry-ready prototypes were made using CAD renderings.</p> 
</div>