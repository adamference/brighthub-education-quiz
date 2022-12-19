---
title: test quiz 23
date: 2022-12-19T13:34:07.104Z
draft: false
featured: false
image:
  filename: featured
  focal_point: Smart
  preview_only: false
---
<script>
let correctAnswer = document.querySelectorAll(".quizbox-question");
for(let i = 0; i < correctAnswer.length; i++) {
  correctAnswer[i].addEventListener("click", function(){
    if(correctAnswer[i].textContent === "hidden answer"){
      correctAnswer[i].style.backgroundColor = "#32dc66";
    }
    else{
      correctAnswer[i].style.backgroundColor = "#dc3232";
    }
  });
}
</script>

<div class="quizbox">
<h2 style="color: #ffffff;">Question 1</h2>
<p>What are some activities that parents can do with their children at home?</p>

<div class="quizbox-question" onclick="this.style.backgroundColor='#32dc66';">Playing board games</div>
<div class="quizbox-question" onclick="this.style.backgroundColor='#dc3232';">Going to the movies</div>
<div class="quizbox-question" onclick="this.style.backgroundColor='#dc3232';">Hiking in the woods</div>
<div class="quizbox-question" onclick="this.style.backgroundColor='#dc3232';">Going to the beach</div>


<p style="text-align: right;"><a href="/parents-children-time-at-home-activities-galore-2/" class="btn btn-primary btn-lg mb-md-1">Next Question <i class="fa-solid fa-arrow-right"></i></a></p>
</div>

<script>
let correctAnswer = document.querySelectorAll(".quizbox-question");
for(let i = 0; i < correctAnswer.length; i++) {
  correctAnswer[i].addEventListener("click", function(){
    if(correctAnswer[i].textContent === "Playing board games"){
      correctAnswer[i].style.backgroundColor = "#32dc66";
      correctAnswer[i].innerHTML = correctAnswer[i].textContent + "<br>Playing board games is a great way for parents and their children to bond and have fun together at home.
    }
    else{
      correctAnswer[i].style.backgroundColor = "#dc3232";
    }
  });
}
</script>