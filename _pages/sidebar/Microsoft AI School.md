---
title: <img src="../images/ImgFile/mms.png" width="500" height="500" referrerpolicy="no-referrer" alt="s1">
permalink: /Microsoft AI School/
layout: single
author_profile: false
sidebar_main: true
---


<html lang="ko">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.1.0/css/all.min.css">
  <style>
    * {
      box-sizing: border-box;
    }
    body {
      font-family: 'San Francisco', 'Helvetica Neue', Helvetica, Arial, sans-serif;
      margin: 0;
      padding: 0;
    }
    .list__item {
      position: relative;
      background-color: #fff;
      border: none;
      border-radius: 5px;
      padding: 20px;
      margin: 20px auto;
      width: 90%;
      max-width: 800px;
      box-shadow: 0 1px 3px rgba(0, 0, 0, 0.12), 0 1px 2px rgba(0, 0, 0, 0.24);
      transition: all 0.3s cubic-bezier(0.25, 0.8, 0.25, 1);
    }
    .list__item:hover {
      box-shadow: 0 14px 28px rgba(0, 0, 0, 0.25), 0 10px 10px rgba(0, 0, 0, 0.22);
    }
    .list__item h2 {
      font-size: 24px;
      margin-bottom: 10px;
      margin-top: 0px;
      color: #333;
      display: inline-block;
    }
    .posts-count {
      display: inline-block;
      /* border: 1px solid #515151; */
      color: #515151;
      font-size: 12px;
      padding: 2px 5px;
      margin-left: 3px;
    }
    .toggle {
      position: absolute;
      top: 20px;
      right: 20px;
      background: none;
      border: none;
      padding: 0;
      margin: 0;
      cursor: pointer;
      font-size: 16px;
      color: #007bff;
      display: inline-block;
    }
    .archive__container {
      max-height: 0;
      overflow: hidden;
      transition: max-height 0.3s ease-out;
      /* 변경: 추가된 코드 */
      overflow: auto;
    }
    .list__item.open .archive__container {
      max-height: 500px;
      transition: max-height 0.5s ease-in;
    }
    .archive__item {
      padding: 0;
      margin-bottom: 5px; /* 간격 수정 */
      clear: both;
      opacity: 0;
      max-height: 0;
      overflow: hidden;
      transition: opacity 0.3s ease-out, max-height 0.3s ease-out;
    }
    .archive__item-title {
      font-size: 20px;
      font-weight: 600;
      margin-bottom: 0; /* 수정: 마진 제거 */
      padding: 0; /* 수정: 패딩 제거 */
      color: #333;
    }
    .archive__item-title a {
      display: inline; /* 수정: 인라인으로 변경 */
      color: #007aff;
      text-decoration: none;
      padding: 0; /* 패딩 수정 */
      margin: 0; /* 마진 수정 */
    }
    .archive__item-title a:hover {
      text-decoration: underline;
    }
    .page__meta-date {
      font-size: 14px;
    }
    .page__meta-date {
      font-size: 14px;
      color: #777;
    }
    .subcategory {
      font-size: 20px;
      font-weight: 600;
      margin-bottom: 5px;
      padding: 10px 0;
      color: #333;
      cursor: pointer;
    }
    .subcategory:hover {
      text-decoration: underline;
    }
    .archive__item-wrapper {
      padding: 10px 0;
    }
    .subcategory-text {
      font-size: 12px;
      color: #e6c129;
      margin-left: 3px;
    }
    .ms-ai-link {
      color: black;
      text-decoration: none;
    }
    .ms-ai-link:visited {
      color: black;
    }
  </style>
</head>

<body>
<h3 style="color: black; text-align: center;"><a class="ms-ai-link" href="https://github.com/potettang/Microsoft-AI-School"><i class="fab fa-github" style="font-size: 1.2em;"></i> MS AI School Github Repository</a></h3>
<br/>

<div class="list__item">
  <h2>CNN Theory Learning<span class="posts-count">📂 4</span></h2>
  <button class="toggle"><img src="../images/ImgFile/lock.png" style="height: 37px; width: auto; margin-top: -4px;" alt="C/C++/C# 이미지"></button>
</div>

<div class="list__item">
  <h2>Artificial Neural Network Theory Learning <span class="posts-count">📂 3</span></h2>
  <button class="toggle"><img src="../images/ImgFile/lock.png" style="height: 37px; width: auto; margin-top: -4px;" alt="C/C++/C# 이미지"></button>
</div>


<div class="list__item">
  <h2>Data Processing Project <span class="posts-count">📂 3</span></h2>
  <button class="toggle"><img src="../images/ImgFile/lock.png" style="height: 37px; width: auto; margin-top: -4px;" alt="C/C++/C# 이미지"></button>
</div>




<div class="list__item">
  <h2>Data Labeling, Image Processing, and Dataset Implementation <span class="posts-count">📂 5</span></h2>
  <button class="toggle"><img src="../images/ImgFile/lock.png" style="height: 37px; width: auto; margin-top: -4px;" alt="C/C++/C# 이미지"></button>
</div>



<div class="list__item">
  <h2>Handling Images and Building Datasets <span class="posts-count">📂 5</span></h2>
  <button class="toggle"><img src="../images/ImgFile/lock.png" style="height: 37px; width: auto; margin-top: -4px;" alt="C/C++/C# 이미지"></button>
</div>



<div class="list__item">
  <h2>Statistics-based Data Analysis <span class="posts-count">📂 8</span></h2>
  <button class="toggle"><img src="../images/ImgFile/lock.png" style="height: 37px; width: auto; margin-top: -4px;" alt="C/C++/C# 이미지"></button>
</div>






<script>
  const listItems = document.querySelectorAll('.list__item');
  listItems.forEach(function(listItem) {
    const toggleButton = listItem.querySelector('.toggle');
    toggleButton.addEventListener('click', function() {
      listItem.classList.toggle('open');
    });
  });

  // 세부 카테고리 관련 코드 제거
  const archiveItems = document.querySelectorAll('.archive__item');
  archiveItems.forEach(function(archiveItem) {
    archiveItem.style.transition = 'opacity 0.5s ease-out, max-height 0.5s ease-out';
    archiveItem.style.maxHeight = '0';
    archiveItem.style.opacity = '0';
  });

  const toggleButtons = document.querySelectorAll('.toggle');
  toggleButtons.forEach(function(toggleButton) {
    toggleButton.addEventListener('click', function() {
      const archiveContainer = toggleButton.parentElement.querySelector('.archive__container');
      const archiveItems = archiveContainer.querySelectorAll('.archive__item');
      
      archiveItems.forEach(function(archiveItem) {
        if (archiveItem.style.maxHeight === '0px' || archiveItem.style.maxHeight === '') {
          archiveItem.style.transition = 'opacity 0.5s ease-in, max-height 0.5s ease-in';
          archiveItem.style.maxHeight = '500px';
          archiveItem.style.opacity = '1';
        } else {
          archiveItem.style.transition = 'opacity 0.5s ease-out, max-height 0.5s ease-out';
          archiveItem.style.maxHeight = '0';
          archiveItem.style.opacity = '0';
        }
      });
    });
  });
</script>
</body>
</html>