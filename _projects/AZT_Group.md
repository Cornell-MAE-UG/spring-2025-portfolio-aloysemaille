---
layout: project
title: QUANTUM RESEARCH
description: Research
technologies: [Clean Room, Experimental tools]
image: /assets/images/ZT6.png
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
    '{{ site.baseurl }}/assets/images/ZT1.png',
    '{{ site.baseurl }}/assets/images/ZT2.png',
    '{{ site.baseurl }}/assets/images/ZT3.png',
    '{{ site.baseurl }}/assets/images/ZT4.png',
    '{{ site.baseurl }}/assets/images/ZT5.png',
    '{{ site.baseurl }}/assets/images/ZT6.png',
    '{{ site.baseurl }}/assets/images/ZT10.png',
    '{{ site.baseurl }}/assets/images/ZT9.png'
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

  // Optional: Auto-slide every 3 seconds
  //setInterval(nextSlide, 3000);
</script>

<div>   
<p>I am part of the AFOSR Sub-team. My work as primarly focused on Qubits and resonators fabrication process design and implementation, as well as research on the impact of 2D-materials on phonon decoherence in quantum devices. I am trained and certified for CNF cleanroom access where I primarly perform my work.</p> 

<p>I am proficient in advanced fabrication techniques including optical and electron-beam photolithography processes (spinning, baking, HDMS oven primer, ABM and SÜSS aligner, JEOL 6300), dry transfer of 2D materials, and reactive ion etching (RIE). I am also proficient in using AJA sputtering systems and the AJA ATC 1800-HY tool for sputtering, ion milling, and controlled oxidation. I can perform measurements with the Everbeing DC Probe Station and the KLA P7 profilometer, as well as any optical microscope and associated imaging/analysis software for nanoscale device inspection and alignment. Other trainings I acquired are micro-bonding, hysical Properties Measurement System (PPMS) and dry transfer.</p>

<p>I was awarded the Summer 2025 Research Award, funded by Boeing. I also got the wonderful opportunity to be featured on Cornell Engineering media.<a href="https://www.linkedin.com/posts/cornell-engineering_aloyse-maille-27-fabricates-quantum-resonators-activity-7370826875004198935-8iyo?utm_source=share&utm_medium=member_desktop&rcm=ACoAAETesJYBOvL9oqfU1LiZcU4lG65tGHJjiYM" target="_blank">See featuring here!</a></p>

<p>Since joining the lab in September 2023, I gained a lot of autonomy on the projects and now have almost complete freedom on the design of the fabrication process design of the qubits, on which I work closely with Joyce Christiansen-Salameh - my mentor since I joined, in Chicago since last winter - and Simon Shi - who joined the project this summer and to whom I got to share my previous experience with optical photolithography and etching processes -, both graduate students working towards PhD.</p>
</div>