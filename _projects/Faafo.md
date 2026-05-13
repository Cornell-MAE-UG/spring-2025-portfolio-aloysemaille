---
layout: project
title: FAAFO
description: Mechatronics Robot competition
technologies: [Robot building, C, arduino programming, color sensor, robot competition, robot motorization, robot design]
image: /assets/images/Faafo1.JPG
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
    '{{ site.baseurl }}/assets/images/Faafo1.JPG',
    '{{ site.baseurl }}/assets/images/Faafo2.HEIC',
    '{{ site.baseurl }}/assets/images/Faafo3.JPG',
    '{{ site.baseurl }}/assets/images/Faafo4.JPG',
    '{{ site.baseurl }}/assets/images/Faafo5.JPG',
    '{{ site.baseurl }}/assets/images/Faafo6.JPG'
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
<p>This is the final project of MAE 3780: Mechatronics, which consisted in a robot competition. Specifically, the goal was to capture more than the opponent on a bicolor field.</p>
</div>

<div>
<p>The driving factor behind FAAFO’s strategy is speed, simplicity, and to not be impacted or depend upon the strategy chosen by the opponent. We prioritized having simple and straightforward mechanisms and code, to improve our reliability and reduce the risk of failure during competition.  </p>
</div>

<div>
<p>The robot’s path during competition was hardcoded and was designed to let us quickly reach the center of the board, collect a majority of the blocks, and then move to a safer and more secluded part of the board to hide from the other robot and avoid any interference. Specifically, our robot’s strategy was to begin located at the center of our board, drive forward at a slight diagonal to the center (to try to avoid robots that drove directly forward in the center), and then turn to the left to align with the center line. The robot then drove forward to the boundary of the board while collecting cubes, before turning to the right and driving forward to stop at the end of the board on the opponent’s side. 


The same simplicity-focused mindset was applied to the design of the arms. They are lightweight, since they are made of cardboard, and are fixed to the robot via loose hinges at a vertical angle so that they are calibrated to fall as soon as the robot starts moving. To help the arms fall forward, a very short backwards motion was added at the beginning of our code. 

Another main aspect that was taken into consideration, was the storage of the cubes after collection. For that purpose, and to achieve a slightly higher robot speed, we designed 3D-printed extensions made to be clipped directly onto the provided wheels. This allowed us to create a protected storage space underneath our robot. To prevent cubes from interfering with the wheels and the rolling ball, we added a “cage” component underneath our chassis, made from cardboard, which both helped contain the cubes and prevented them from running into the wheels.

During this project, I took charge of the wiring, the code and the decoration of our robot. I also participating in assembling the wheels and its main body.
</p>
</div>

<div>
<p>
#include <avr/io.h>
#include <util/delay.h>


int main(void){ // setup code that only runs once
  DDRB |= 0b00000011;// set pins 8 and 9 as outputs for "right" motor
  DDRB |= 0b00001100;// set pins 10 and 11 as outputs for "left" motor


  while(1){ // code that loops forever
   if (PINB & 0b00010000){ // when switch on, follow pattern by calling functions
     drive_forward(200);
     drive_backward(2600);
     drive_left(500);
     drive_backward(2200);
     drive_right(550);
     drive_backward(2500);
     stop(500000);
   }
   else {
   } } }


// delay function and moving/stopping functions
void delay_ms(int ms) {
   while (ms--) {
       _delay_ms(1);
   } }


void drive_forward(int t){
   PORTB |= 0b00001001;
   delay_ms(t);
   PORTB &=~ 0b00001001;
}
void drive_backward(int t){
   PORTB |= 0b00000110;
   delay_ms(t);
   PORTB &=~ 0b00000110;
}
void drive_left(int t){
   PORTB |= 0b00000101;
   delay_ms(t);
   PORTB &=~ 0b00000101;
}
void drive_right(int t){
   PORTB |= 0b00001010;
   delay_ms(t);
   PORTB &=~ 0b00001010;
}
void stop(int t){
   PORTB &=~ 0b00001111;
   delay_ms(t); }

The code above was used for the competition.</p> 
</div>

<div>
<p>This work was conducted in collaboration with Jessica Racozky and Kaila Danielson, Cornell Mechanical Engineering Students.</p> 
</div>


