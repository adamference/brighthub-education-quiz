---
title: test with hidden slides
date: 2022-12-20T04:12:04.186Z
draft: false
featured: false
image:
  filename: featured
  focal_point: Smart
  preview_only: false
---

  <div class="slides">
    <div class="slide active" id="slide1">

<div class="quizbox">
<h2 style="color: #ffffff;">Question 1</h2>
<p>Quiz Question Here</p>

<div id="quizbox-question" class="quizbox-question" onclick="document.getElementById('hidden-answer').style.display='block';"><a href="#quizbox-question">multiple choice</a></div>
<div id="quizbox-question" class="quizbox-question" onclick="document.getElementById('hidden-answer').style.display='block';"><a href="#quizbox-question">multiple choice</a></div>
<div id="quizbox-question" class="quizbox-question" onclick="document.getElementById('hidden-answer').style.display='block';"><a href="#quizbox-question">multiple choice</a></div>
<div id="quizbox-question" class="quizbox-question" onclick="document.getElementById('hidden-answer').style.display='block';"><a href="#quizbox-question">multiple choice</a></div>

<div ID="hidden-answer" style="display:none;">hidden answer</div>
    </div>

 <div class="slide" id="slide2">
<div class="quizbox">
<h2 style="color: #ffffff;">Question 2</h2>
<p>Quiz Question Here</p>

<div id="quizbox-question" class="quizbox-question" onclick="document.getElementById('hidden-answer').style.display='block';"><a href="#quizbox-question">multiple choice</a></div>
<div id="quizbox-question" class="quizbox-question" onclick="document.getElementById('hidden-answer').style.display='block';"><a href="#quizbox-question">multiple choice</a></div>
<div id="quizbox-question" class="quizbox-question" onclick="document.getElementById('hidden-answer').style.display='block';"><a href="#quizbox-question">multiple choice</a></div>
<div id="quizbox-question" class="quizbox-question" onclick="document.getElementById('hidden-answer').style.display='block';"><a href="#quizbox-question">multiple choice</a></div>

<div ID="hidden-answer" style="display:none;">hidden answer</div>
    </div>

    <div class="slide" id="slide3">
<div class="quizbox">
<h2 style="color: #ffffff;">Question 3</h2>
<p>Quiz Question Here</p>

<div id="quizbox-question" class="quizbox-question" onclick="document.getElementById('hidden-answer').style.display='block';"><a href="#quizbox-question">multiple choice</a></div>
<div id="quizbox-question" class="quizbox-question" onclick="document.getElementById('hidden-answer').style.display='block';"><a href="#quizbox-question">multiple choice</a></div>
<div id="quizbox-question" class="quizbox-question" onclick="document.getElementById('hidden-answer').style.display='block';"><a href="#quizbox-question">multiple choice</a></div>
<div id="quizbox-question" class="quizbox-question" onclick="document.getElementById('hidden-answer').style.display='block';"><a href="#quizbox-question">multiple choice</a></div>

<div ID="hidden-answer" style="display:none;">hidden answer</div>

    </div>
  </div>

    <div class="slide" id="slide4">
<div class="quizbox">
<h2 style="color: #ffffff;">Question 4</h2>
<p>Quiz Question Here</p>

<div id="quizbox-question" class="quizbox-question" onclick="document.getElementById('hidden-answer').style.display='block';"><a href="#quizbox-question">multiple choice</a></div>
<div id="quizbox-question" class="quizbox-question" onclick="document.getElementById('hidden-answer').style.display='block';"><a href="#quizbox-question">multiple choice</a></div>
<div id="quizbox-question" class="quizbox-question" onclick="document.getElementById('hidden-answer').style.display='block';"><a href="#quizbox-question">multiple choice</a></div>
<div id="quizbox-question" class="quizbox-question" onclick="document.getElementById('hidden-answer').style.display='block';"><a href="#quizbox-question">multiple choice</a></div>

<div ID="hidden-answer" style="display:none;">hidden answer</div>

    </div>
  </div>

    <div class="slide" id="slide5">
<div class="quizbox">
<h2 style="color: #ffffff;">Question 5</h2>
<p>Quiz Question Here</p>

<div id="quizbox-question" class="quizbox-question" onclick="document.getElementById('hidden-answer').style.display='block';"><a href="#quizbox-question">multiple choice</a></div>
<div id="quizbox-question" class="quizbox-question" onclick="document.getElementById('hidden-answer').style.display='block';"><a href="#quizbox-question">multiple choice</a></div>
<div id="quizbox-question" class="quizbox-question" onclick="document.getElementById('hidden-answer').style.display='block';"><a href="#quizbox-question">multiple choice</a></div>
<div id="quizbox-question" class="quizbox-question" onclick="document.getElementById('hidden-answer').style.display='block';"><a href="#quizbox-question">multiple choice</a></div>

<div ID="hidden-answer" style="display:none;">hidden answer</div>

    </div>
  </div>


<p style="float:left;"><button id="next-btn" class="btn btn-primary btn-lg mb-md-1">Next Question <i class="fa-solid fa-arrow-right"></i></button></p>
<p style="text-align: right;"><button id="next-btn" class="btn btn-primary btn-lg mb-md-1">Next Question <i class="fa-solid fa-arrow-right"></i></button></p>
</div>


<script>
  document.addEventListener("DOMContentLoaded", function(){
    // Get our elements
    var slides = document.querySelectorAll(".slide");
    var prevBtn = document.getElementById("prev-btn");
    var nextBtn = document.getElementById("next-btn");
    // Current Slide
    var currentSlide = 0;

    // Show slide function
    function showSlide(n){
      // Remove active class from all slides
      slides.forEach(function(slide){
        slide.classList.remove("active");
      });
      // Add active class to the current slide
      slides[n].classList.add("active");
    }

    // Next slide function
    function nextSlide(){
      currentSlide++;
      if(currentSlide > slides.length -1) {
        currentSlide = 0;
      }
      showSlide(currentSlide);
    }

    // Previous slide function
    function prevSlide(){
      currentSlide--;
      if(currentSlide < 0) {
        currentSlide = slides.length -1;
      }
      showSlide(currentSlide);
    }

    // Ajax call for next slide
    function nextSlideAjax(){
      var xhttp = new XMLHttpRequest();
      xhttp.onreadystatechange = function() {
        if (this.readyState == 4 && this.status == 200) {
            nextSlide();
        }
      };
      xhttp.open("GET", "/nextslide", true);
      xhttp.send();
    }

    // Ajax call for previous slide
    function prevSlideAjax(){
      var xhttp = new XMLHttpRequest();
      xhttp.onreadystatechange = function() {
        if (this.readyState == 4 && this.status == 200) {
            prevSlide();
        }
      };
      xhttp.open("GET", "/previousslide", true);
      xhttp.send();
    }

    // Button events
    nextBtn.addEventListener("click", nextSlideAjax);
    prevBtn.addEventListener("click", prevSlideAjax);

  });
</script>
