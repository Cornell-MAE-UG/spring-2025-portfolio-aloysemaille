---
layout: project
title: NASA L'SPACE
description: Semester long academy 
technologies: [JMARS, NX Siemens CAD, Risk Management, Project Management, Heat Transfer, TRL, Systems, Teamwork, Requirements, N-Chart, Risk Matrix, Science Objectives]
image: /assets/images/MCA3.png
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
    '{{ site.baseurl }}/assets/images/CertificateLspace.jpg',
    '{{ site.baseurl }}/assets/images/MCA1.png',
    '{{ site.baseurl }}/assets/images/MCA2.png',
    '{{ site.baseurl }}/assets/images/MCA3.png',
    '{{ site.baseurl }}/assets/images/MCA4.png',
    '{{ site.baseurl }}/assets/images/MCA5.png',
    '{{ site.baseurl }}/assets/images/MCA6.png',
    '{{ site.baseurl }}/assets/images/MCA7.png',
    '{{ site.baseurl }}/assets/images/MCA0.png'
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
<p> During the Spring 2025, I completed NASA's L'SPACE Program's MCA Academy. </p>

<p> My primary roles were Lead Systems Engineer and Mission Outreach Officer. </p> 

<p> This academy consisted of weekly online lectures, as well as remotely working together with an amazing team on the first steps of a project: the Concept and Technology Development phase and the Preliminary Design and Technology Completion phase. </p>

<p> Our Mission Task consisted in gaining understanding on Venus and the interaction between its surface and atmosphere, with the use of an Aerobot System. We learned to use NASA’s tools to define science objective, risks and requirements, but also mission location, concept of operations and the programmatic, science and engineering components of the mission. Some of those newly acquired skills are certified by Skill Badges displayed on my certificate (Teaming, Requirements, Risk Management, Project Management, Systems, Heat Transfer, Siemens NX CAD).</p>    
</div>

