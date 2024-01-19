<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>University Complaint Form</title>
  <style>
    body {
      font-family: Arial, sans-serif;
    }
    .center {
      text-align: center;
      color: green;
    }
    .complain-text {
      text-align: center;
      color: black;
      font-weight: bold;
      font-size: 18px;
    }
    .form-container {
      max-width: 400px;
      margin: auto;
      padding: 20px;
    }
    #video-container {
      display: none;
      text-align: center;
    }
  </style>
</head>
<body>

<div class="center">
  <h1>HNB GARHWAL UNIVERSITY</h1>
</div>

<div class="complain-text">
  <p>Complain here Regarding Copy check</p>
</div>

<div class="form-container">
  <form id="complaintForm" action="#" method="post" onsubmit="showVideo(event)">
    <b><label for="name">Enter your name:</label><br>
    <input type="text" id="name" name="name" required><br></b>

    <b><label for="rollNo">Enter your roll no:</label><br>
    <input type="text" id="rollNo" name="rollNo" required><br></b>

    <br><input type="submit" value="Submit">
  </form>
</div>

<div id="video-container">
  <video width="560" height="315" controls loop>
    <source src="video.html.mp4" type="video/mp4">
    Your browser does not support the video tag.
  </video>
</div>

<script>
  function showVideo(event) {
    event.preventDefault(); // Prevent the form from submitting
    document.getElementById("complaintForm").style.display = "none";
    var videoContainer = document.getElementById("video-container");
    videoContainer.style.display = "block";

    // Get the video element inside the video container
    var video = videoContainer.querySelector("video");

    // Attempt to play the video
    video.play();
  }
</script>

</body>
</html>
