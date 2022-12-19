---
title: Quiz coded
date: 2022-12-19T06:52:23.748Z
draft: false
featured: false
image:
  filename: featured
  focal_point: Smart
  preview_only: false
---
<style>
.red {
  color: red;
}
.green {
  color: green;
}
</style>
</head>
<body>

<h2>Question 1</h2>
Which of the following is an example of a word formation process?
<p>
<input type="radio" name="q1" onclick="myFunction(this.value)" value="A"> Adding a suffix<br>
<input type="radio" name="q1" onclick="myFunction(this.value)" value="B"> Replacing a letter<br>
<input type="radio" name="q1" onclick="myFunction(this.value)" value="C"> Adding a prefix<br>
<input type="radio" name="q1" onclick="myFunction(this.value)" value="D"> All of the above
</p>
<h2>Question 2</h2>
Which of the following is an example of a word conversion process?
<p>
<input type="radio" name="q2" onclick="myFunction(this.value)" value="A"> Adding a suffix<br>
<input type="radio" name="q2" onclick="myFunction(this.value)" value="B"> Replacing a letter<br>
<input type="radio" name="q2" onclick="myFunction(this.value)" value="C"> Adding a prefix<br>
<input type="radio" name="q2" onclick="myFunction(this.value)" value="D"> Changing an adjective to a noun
</p>
<script>
function myFunction(val) {
  if (val == "D") {
    document.getElementById("demo").className = "green";
  } else {
    document.getElementById("demo").className = "red";
  }
}
</script>