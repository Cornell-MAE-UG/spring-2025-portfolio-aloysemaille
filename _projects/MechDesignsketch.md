---
layout: project
title: MECHANICAL DESIGN SKETCHES AND CAD
description: Mech design favorites
technologies: [MATLAB, State-Space models, Block Diagram, PD Control, requirements]
image: /assets/images/MD0.png
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
    '{{ site.baseurl }}/assets/images/MD1sk.png',
    '{{ site.baseurl }}/assets/images/MD2sk.png',
    '{{ site.baseurl }}/assets/images/MD3sk.png',
    '{{ site.baseurl }}/assets/images/MD4sk.JPG',
    '{{ site.baseurl }}/assets/images/MD5sk.JPG',
    '{{ site.baseurl }}/assets/images/MD6sk.JPG'
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
<p>This is a collection of my favorite works in mechanical design</p>
</div>
