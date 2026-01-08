---
layout: project
title: NORTH STAR - POINTING CONTROL FOR SATELLITES
description: System Dynamics Final Project
technologies: [MATLAB, State-Space models, Block Diagram, PD Control, requirements]
image: /assets/images/SD7.png
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
    '{{ site.baseurl }}/assets/images/SD1.png',
    '{{ site.baseurl }}/assets/images/SD2.png',
    '{{ site.baseurl }}/assets/images/SD3.png',
    '{{ site.baseurl }}/assets/images/SD4.png',
    '{{ site.baseurl }}/assets/images/SD5.png',
    '{{ site.baseurl }}/assets/images/SD6.png'
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
<p>This is the final groupwork of MAE 3260: System Dynamics, which consisted in understanding the control system and the functionning of a chosen real life system.</p>
    
<p>The system our team decided to study is a satellite located in a geostationary orbit pointing at a static location on the Earth surface. It was selected as it is a common interest to all of our group members to understand better how pointing or attitude control in a satellite operates. Those systems can have a lot of applications, from commercial purposes to research and defense, and even if we don’t actively work with such systems in the future, we still use them directly or indirectly in our daily lives. They are used for radio and television communications but can also now be used for messaging on our phones and other fun things.</p>

<p>In the context of that project, I worked on the development of the state space models and block diagrams of the satellite pointing control system. I developed a simplified disturbance model of the satellite and participated in the performance requirement parameters design, as well as in the MATLAB modelization of the system.</p> 
</div>

<div>
<p>This work was conducted in collaboration with Olivia Lee, Ethan Kim and Benjamin Okoronkwo, Cornell Mechanical Engineering Students.</p> 
</div>