---
title: "People"
layout: single
permalink: /people/
author_profile: true
---

<!-- <input type="text" id="peopleSearch" onkeyup="searchPeople()" placeholder="Search by name or role..." style="width: 100%; padding: 12px; margin-bottom: 25px; border: 1px solid #ddd; border-radius: 4px; font-size: 16px;"> -->

<div id="peopleGrid">

  <!-- <h2 class="archive__subtitle">Post docs and graduate students</h2> -->
  <h2 style="color: #333; font-weight: bold; border-bottom: 2px solid #eee; padding-bottom: 10px;">Post docs and graduate students</h2>
  <div class="people-row" style="display: flex; flex-wrap: wrap; gap: 30px;">
    
    <div class="person-card" style="width: 180px; text-align: center;">
      <img src="/images/Koby_Amsalem.jpg" alt="Koby Amsalem" style="border-radius: 50%; width: 130px; height: 130px; object-fit: cover; margin-bottom: 10px;">
      <div style="font-weight: bold; text-decoration: underline;">Koby Amsalem</div>
      <div style="font-size: 0.85em; color: #666;">PhD Student</div>
    </div>

    <div class="person-card" style="width: 180px; text-align: center;">
      <img src="/images/Renata_Olive.jpg" alt="Renata Olive" style="border-radius: 50%; width: 130px; height: 130px; object-fit: cover; margin-bottom: 10px;">
      <div style="font-weight: bold; text-decoration: underline;">Renata Olive</div>
      <div style="font-size: 0.85em; color: #666;">PhD Student</div>
    </div>

    <div class="person-card" style="width: 180px; text-align: center;">
      <img src="/images/Guy_Priebatch.jpg" alt="Renata Olive" style="border-radius: 50%; width: 130px; height: 130px; object-fit: cover; margin-bottom: 10px;">
      <div style="font-weight: bold; text-decoration: underline;">Renata Olive</div>
      <div style="font-size: 0.85em; color: #666;">M.Sc. Student</div>
    </div>

      <div class="person-card" style="width: 180px; text-align: center;">
      <img src="/images/Eli_Yovel.jpg" alt="Eli Yovel" style="border-radius: 50%; width: 130px; height: 130px; object-fit: cover; margin-bottom: 10px;">
      <div style="font-weight: bold; text-decoration: underline;">Eli Yovel</div>
      <div style="font-size: 0.85em; color: #666;">M.Sc. Student</div>
    </div>

    <div class="person-card" style="width: 180px; text-align: center;">
      <img src="/images/Karine_Sacagiu.jpg" alt="Karine Sacagiu" style="border-radius: 50%; width: 130px; height: 130px; object-fit: cover; margin-bottom: 10px;">
      <div style="font-weight: bold; text-decoration: underline;">Karine Sacagiu</div>
      <div style="font-size: 0.85em; color: #666;">M.Sc. Student</div>
    </div>

    <div class="person-card" style="width: 180px; text-align: center;">
      <img src="/images/Yonatan_Markman.jpeg" alt="Yonatan Markman" style="border-radius: 50%; width: 130px; height: 130px; object-fit: cover; margin-bottom: 10px;">
      <div style="font-weight: bold; text-decoration: underline;">Yonatan Markman</div>
      <div style="font-size: 0.85em; color: #666;">M.Sc. Student</div>
    </div>
  </div>
</div>


<h2 style="color: #333; font-weight: bold; border-bottom: 2px solid #eee; padding-bottom: 10px; margin-top: 50px;">Alumni</h2>
<div class="alumni-section" style="margin-top: 20px; line-height: 1.8;">
  <ul style="list-style-type: none; padding-left: 0;">
    <li><strong>Dr. Jane Doe</strong> - Post-doc (2022-2024)</li>
    <li><strong>John Smith</strong> - M.Sc. Student (2021-2023)</li>
  </ul>
</div>

<!-- <script>
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
</script> -->