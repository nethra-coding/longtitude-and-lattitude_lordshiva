<!DOCTYPE html>
<html>
<body>

<style>
body { text-align: center; } </style>

<p align=center>Click the button to get your coordinates.</p>

<p align=center>

<button onclick="getLocation()"><img src = "https://img.shields.io/badge/Coordinates-longitude%20and%20%20latitude%20-orange"</img></button>

<p id="demo"></p>

<script align=center>
var x = document.getElementById("demo");

function getLocation() {
  if (navigator.geolocation) {
    navigator.geolocation.getCurrentPosition(showPosition);
  } else { 
    x.innerHTML = "Geolocation is not supported by this browser.";
  }
}

function showPosition(position) {
  x.innerHTML = "Latitude: " + position.coords.latitude + 
  "<br>Longitude: " + position.coords.longitude;
}
</script>

</body>
</html>
