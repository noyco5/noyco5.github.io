---
title: "People"
layout: single
permalink: /people/
author_profile: true
---

<input type="text" id="peopleSearch" onkeyup="searchPeople()" placeholder="Search by name or role..." style="width: 100%; padding: 12px; margin-bottom: 25px; border: 1px solid #ddd; border-radius: 4px; font-size: 16px;">

<div id="peopleGrid">

  <h2 class="archive__subtitle">Post docs and graduate students</h2>
  <div class="people-row" style="display: flex; flex-wrap: wrap; gap: 30px;">
    
    <div class="person-card" style="width: 180px; text-align: center;">
      <img src="Koby_Amsalem.jpg" alt="Koby Amsalem" style="border-radius: 50%; width: 130px; height: 130px; object-fit: cover; margin-bottom: 10px;">
      <div style="font-weight: bold; text-decoration: underline;">Koby Amsalem</div>
      <div style="font-size: 0.85em; color: #666;">PhD Student</div>
    </div>

    <div class="person-card" style="width: 180px; text-align: center;">
      <img src="Renata_Olive.jpg" alt="Tal Hanuhov" style="border-radius: 50%; width: 130px; height: 130px; object-fit: cover; margin-bottom: 10px;">
      <div style="font-weight: bold; text-decoration: underline;">Renata Olive</div>
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