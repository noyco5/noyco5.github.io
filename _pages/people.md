---
title: "People"
layout: single
permalink: /people/
author_profile: true
---

<input type="text" id="peopleSearch" onkeyup="searchPeople()" placeholder="Search by name or role..." style="width: 100%; padding: 12px; margin-bottom: 25px; border: 1px solid #ddd; border-radius: 4px; font-size: 16px;">

<div id="peopleGrid">

  <h2 class="archive__subtitle">Principal Investigator</h2>
  <div class="people-row" style="display: flex; flex-wrap: wrap; gap: 20px; margin-bottom: 40px;">
    <div class="person-card" style="width: 200px; text-align: center;">
      <img src="/images/noy_cohen.jpg" alt="Noy Cohen" style="border-radius: 50%; width: 150px; height: 150px; object-fit: cover; margin-bottom: 10px;">
      <div style="font-weight: bold;">Noy Cohen</div>
      <div style="font-size: 0.9em; color: #666;">Associate Professor</div>
    </div>
  </div>

  <h2 class="archive__subtitle">Students</h2>
  <div class="people-row" style="display: flex; flex-wrap: wrap; gap: 30px;">
    
    <div class="person-card" style="width: 180px; text-align: center;">
      <img src="/images/mariana_levin.jpg" alt="Mariana Levin" style="border-radius: 50%; width: 130px; height: 130px; object-fit: cover; margin-bottom: 10px;">
      <div style="font-weight: bold; text-decoration: underline;">Mariana Levin</div>
      <div style="font-size: 0.85em; color: #666;">PhD Student</div>
    </div>

    <div class="person-card" style="width: 180px; text-align: center;">
      <img src="/images/tal_hanuhov.jpg" alt="Tal Hanuhov" style="border-radius: 50%; width: 130px; height: 130px; object-fit: cover; margin-bottom: 10px;">
      <div style="font-weight: bold; text-decoration: underline;">Tal Hanuhov</div>
      <div style="font-size: 0.85em; color: #666;">PhD Student</div>
    </div>

    <div class="person-card" style="width: 180px; text-align: center;">
      <img src="/images/renata_olive.jpg" alt="Renata Olive" style="border-radius: 50%; width: 130px; height: 130px; object-fit: cover; margin-bottom: 10px;">
      <div style="font-weight: bold; text-decoration: underline;">Renata Olive</div>
      <div style="font-size: 0.85em; color: #666;">PhD Student</div>
    </div>

  </div>
</div>

<script>
function searchPeople() {
  var input = document.getElementById('peopleSearch');
  var filter = input.value.toUpperCase();
  var cards = document.getElementsByClassName('person-card');

  for (var i = 0; i < cards.length; i++) {
    var txtValue = cards[i].textContent || cards[i].innerText;
    if (txtValue.toUpperCase().indexOf(filter) > -1) {
      cards[i].style.display = "";
    } else {
      cards[i].style.display = "none";
    }
  }
}
</script>