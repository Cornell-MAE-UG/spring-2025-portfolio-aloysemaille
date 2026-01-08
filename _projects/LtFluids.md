---
layout: project
title: WEED WHACKER DISSECTION
description: Fluids dissection
technologies: [Venturi, Mechanical Dissection, Physical Tools, Critical Thinking, Teamwork, Creativity]
image: /assets/images/F0.jpg
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
    '{{ site.baseurl }}/assets/images/F0.jpg',
    '{{ site.baseurl }}/assets/images/F1.png',
    '{{ site.baseurl }}/assets/images/F2.png',
    '{{ site.baseurl }}/assets/images/F3.png',
    '{{ site.baseurl }}/assets/images/F4.png',
    '{{ site.baseurl }}/assets/images/F5.png',
    '{{ site.baseurl }}/assets/images/F6.png',
    '{{ site.baseurl }}/assets/images/F7.png',
    '{{ site.baseurl }}/assets/images/F8.png',
    '{{ site.baseurl }}/assets/images/F9.png',
    '{{ site.baseurl }}/assets/images/F10.png',
    '{{ site.baseurl }}/assets/images/F11.png'
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
<p>This is the final groupwork of MAE 3230: Introduction to Fluid Dynamics.</p>

<p>https://youtu.be/3ZLGq0wO1b0</p>
</div>

<div>
<p> In this project, I worked on the weed whacker dissection itself, deconstructing the object in order to understand how it works. I make the block diagram and drew some of the schematics for our presentation. I participated in the uncovering of the principles and the mechanisms of the device. Finally, I participated in the video voice over.</p>
    
<p>This project consisted in the dissection of a fluid device, which in our case was a weed whacker, in order to identify the relevant components and proceed to the fluid analysis of the system.</p>

<p>Several main fluid components where identified in the system such as the carburetor with its Venturi, the flywheel and the piston. Detailed explanations of their functionning and relevant calculations were performed.</p> 
</div>

<div>
<p>Work conducted in collaboration with Jordan Vogel, Kaila Danielson, Natalie Kaplan and Zawad Dewan, Cornell Mechanical Engineering Students.</p> 
</div>