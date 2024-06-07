---
title: <img src="../images/ImgFile/r.png" width="100" height="100" referrerpolicy="no-referrer" alt="s1">
permalink: /R/
layout: single
author_profile: false
sidebar_main: True
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
  </style>
</head>


<body>

<div class="list__item">
  <h2>Programming <span class="posts-count">📂 Total 5 post</span></h2>
  <button class="toggle">View posts</button>
  <div class="archive__container">
    <h3 class="subcategory" data-category="subcategory1">Subcategory <span class="subcategory-text">📁1 posts</span></h3>
    <div class="archive__item-wrapper">
      <article class="archive__item" itemscope="" itemtype="https://schema.org/CreativeWork" data-category="subcategory1">
        <h3 class="archive__item-title no_toc" itemprop="headline">
          <a href="/pythonnote/">pythonnote</a>
        </h3>
        <p class="page__meta">
          <span class="page__meta-date">
            <i class="far fa-calendar-alt" aria-hidden="true"></i>
            <time datetime="2023-03-15T00:00:00+09:00">2023-03-15</time>
          </span>
        </p>
      </article>
    </div>
    <div class="archive__item-wrapper">
      <article class="archive__item" itemscope="" itemtype="https://schema.org/CreativeWork" data-category="subcategory1">
        <h3 class="archive__item-title no_toc" itemprop="headline">
          <a href="/pythonnote/">pythonnote</a>
        </h3>
        <p class="page__meta">
          <span class="page__meta-date">
            <i class="far fa-calendar-alt" aria-hidden="true"></i>
            <time datetime="2023-03-15T00:00:00+09:00">2023-03-15</time>
          </span>
        </p>
      </article>
    </div>
    <div class="archive__item-wrapper">
      <article class="archive__item" itemscope="" itemtype="https://schema.org/CreativeWork" data-category="subcategory1">
        <h3 class="archive__item-title no_toc" itemprop="headline">
          <a href="/pythonnote/">pythonnote</a>
        </h3>
        <p class="page__meta">
          <span class="page__meta-date">
            <i class="far fa-calendar-alt" aria-hidden="true"></i>
            <time datetime="2023-03-15T00:00:00+09:00">2023-03-15</time>
          </span>
        </p>
      </article>
    </div>
    <div class="archive__item-wrapper">
      <article class="archive__item" itemscope="" itemtype="https://schema.org/CreativeWork" data-category="subcategory1">
        <h3 class="archive__item-title no_toc" itemprop="headline">
          <a href="/pythonnote/">pythonnote</a>
        </h3>
        <p class="page__meta">
          <span class="page__meta-date">
            <i class="far fa-calendar-alt" aria-hidden="true"></i>
            <time datetime="2023-03-15T00:00:00+09:00">2023-03-15</time>
          </span>
        </p>
      </article>
    </div>
    <div class="archive__item-wrapper">
      <article class="archive__item" itemscope="" itemtype="https://schema.org/CreativeWork" data-category="subcategory1">
        <h3 class="archive__item-title no_toc" itemprop="headline">
          <a href="#">Programming note</a>
        </h3>
        <p class="page__meta">
          <span class="page__meta-date">
            <i class="far fa-calendar-alt" aria-hidden="true"></i>
            <time datetime="2023-03-15T00:00:00+09:00">2023-03-15</time>
          </span>
        </p>
      </article>
    </div>
    <div class="archive__item-wrapper">
      <article class="archive__item" itemscope="" itemtype="https://schema.org/CreativeWork" data-category="subcategory1">
        <h3 class="archive__item-title no_toc" itemprop="headline">
          <a href="#">Programming note</a>
        </h3>
        <p class="page__meta">
          <span class="page__meta-date">
            <i class="far fa-calendar-alt" aria-hidden="true"></i>
            <time datetime="2023-03-15T00:00:00+09:00">2023-03-15</time>
          </span>
        </p>
      </article>
    </div>
    <div class="archive__item-wrapper">
      <article class="archive__item" itemscope="" itemtype="https://schema.org/CreativeWork" data-category="subcategory1">
        <h3 class="archive__item-title no_toc" itemprop="headline">
          <a href="#">Programming note</a>
        </h3>
        <p class="page__meta">
          <span class="page__meta-date">
            <i class="far fa-calendar-alt" aria-hidden="true"></i>
            <time datetime="2023-03-15T00:00:00+09:00">2023-03-15</time>
          </span>
        </p>
      </article>
    </div>
    <h3 class="subcategory" data-category="subcategory2">Subcategory2 <span class="subcategory-text">📁1 posts</span></h3>
    <div class="archive__item-wrapper">
      <article class="archive__item" itemscope="" itemtype="https://schema.org/CreativeWork" data-category="subcategory2">
        <h3 class="archive__item-title no_toc" itemprop="headline">
          <a href="/pythonnote/">pythonnote</a>
        </h3>
        <p class="page__meta">
          <span class="page__meta-date">
            <i class="far fa-calendar-alt" aria-hidden="true"></i>
            <time datetime="2023-03-15T00:00:00+09:00">2023-03-15</time>
          </span>
        </p>
      </article>
    </div>
  </div>
</div>

<script>
  const listItems = document.querySelectorAll('.list__item');
  listItems.forEach(function(listItem) {
    const toggleButton = listItem.querySelector('.toggle');
    toggleButton.addEventListener('click', function() {
      listItem.classList.toggle('open');
    });
  });

  const subcategories = document.querySelectorAll('.subcategory');
  subcategories.forEach(function(subcategory) {
    subcategory.addEventListener('click', function() {
      const category = subcategory.dataset.category;
      const articles = document.querySelectorAll(`.archive__item[data-category="${category}"]`);

      // Close other subcategories
      subcategories.forEach(function(otherSubcategory) {
        if (otherSubcategory !== subcategory) {
          const otherCategory = otherSubcategory.dataset.category;
          const otherArticles = document.querySelectorAll(`.archive__item[data-category="${otherCategory}"]`);
          otherArticles.forEach(function(article) {
            // 변경: 속도 조절
            article.style.transition = 'opacity 0.5s ease-out, max-height 0.5s ease-out';
            article.style.maxHeight = '0';
            article.style.opacity = '0';
          });
        }
      });

      articles.forEach(function(article) {
        if (article.style.maxHeight === '0px' || article.style.maxHeight === '') {
          // 변경: 속도 조절
          article.style.transition = 'opacity 0.5s ease-in, max-height 0.5s ease-in';
          article.style.maxHeight = '500px';
          article.style.opacity = '1';
        } else {
          // 변경: 속도 조절
          article.style.transition = 'opacity 0.5s ease-out, max-height 0.5s ease-out';
          article.style.maxHeight = '0';
          article.style.opacity = '0';
        }
      });
    });
  });
</script>










<!-- <html lang="ko">
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
      border: 1px solid #515151;
      color: #515151;
      font-size: 14px;
      padding: 2px 5px;
      margin-left: 3px;
    }
    .toggle {
      background: none;
      border: none;
      padding: 0;
      margin: 0;
      cursor: pointer;
      font-size: 16px;
      color: #007bff;
      display: inline-block;
      margin-left: 10px;
    }
    .archive__container {
      max-height: 0;
      overflow: hidden;
      transition: max-height 0.3s ease-out;
    }
    .list__item.open .archive__container {
      max-height: 500px;
      transition: max-height 0.5s ease-in;
    }
    .archive__item {
      padding: 0;
      margin-bottom: 0px;
      clear: both;
      opacity: 0;
      max-height: 0;
      overflow: hidden;
      transition: opacity 0.3s ease-out, max-height 0.3s ease-out;
    }
    .archive__item-title {
      font-size: 20px;
      font-weight: 600;
      margin-bottom: 5px;
      padding: 10px 0;
      color: #333;
    }
    .archive__item-title a {
      display: inline-block;
      width: max-content;
      color: #007aff;
      text-decoration: none;
    }
    .archive__item-title a:hover {
      text-decoration: underline;
    }
    .page__meta-date {
      font-size: 14px;
      color: #777;
    }
    .subcategory {
      font-size: 18px;
      font-weight: 600;
      margin-bottom: 5px;
      padding: 10px 0;
      color: #333;
      cursor: pointer;
    }
    .subcategory:hover {
      text-decoration: underline;
    }
  </style>

<body>

<div class="list__item">
  <h2>Programming <span class="posts-count">2 posts</span></h2>
  <button class="toggle">View posts</button>
  <div class="archive__container">
    <h3 class="subcategory" data-category="subcategory1">Subcategory 1</h3>
    <article class="archive__item" itemscope="" itemtype="https://schema.org/CreativeWork" data-category="subcategory1">
      <h3 class="archive__item-title no_toc" itemprop="headline">
        <a href="/programmingnote/" rel="permalink">Programming note</a>
      </h3>
      <p class="page__meta">
        <span class="page__meta-date">
          <i class="far fa-calendar-alt" aria-hidden="true"></i>
          <time datetime="2023-03-15T00:00:00+09:00">2023-03-15</time>
        </span>
      </p>
    </article>
    <article class="archive__item" itemscope="" itemtype="https://schema.org/CreativeWork" data-category="subcategory1">
      <h3 class="archive__item-title no_toc" itemprop="headline">
        <a href="/programmingnote/" rel="permalink">Programming note</a>
      </h3>
      <p class="page__meta">
        <span class="page__meta-date">
          <i class="far fa-calendar-alt" aria-hidden="true"></i>
          <time datetime="2023-03-15T00:00:00+09:00">2023-03-15</time>
        </span>
      </p>
    </article>
    <h3 class="subcategory" data-category="subcategory2">Subcategory 2</h3>
    <article class="archive__item" itemscope="" itemtype="https://schema.org/CreativeWork" data-category="subcategory2">
      <h3 class="archive__item-title no_toc" itemprop="headline">
        <a href="/anotherprogrammingnote/" rel="permalink">Another Programming note</a>
      </h3>
      <p class="page__meta">
        <span class="page__meta-date">
          <i class="far fa-calendar-alt" aria-hidden="true"></i>
          <time datetime="2023-03-20T00:00:00+09:00">2023-03-20</time>
        </span>
      </p>
    </article>
  </div>
</div>

<script>
  const listItems = document.querySelectorAll('.list__item');
  listItems.forEach(function(listItem) {
    const toggleButton = listItem.querySelector('.toggle');
    toggleButton.addEventListener('click', function() {
      listItem.classList.toggle('open');
    });
  });

  const subcategories = document.querySelectorAll('.subcategory');
  subcategories.forEach(function(subcategory) {
    subcategory.addEventListener('click', function() {
      const category = subcategory.dataset.category;
      const articles = document.querySelectorAll(`.archive__item[data-category="${category}"]`);
      articles.forEach(function(article) {
        if (article.style.maxHeight === '0px' || article.style.maxHeight === '') {
          article.style.maxHeight = '500px';
          article.style.opacity = '1';
        } else {
          article.style.maxHeight = '0';
          article.style.opacity = '0';
        }
      });
    });
  });
</script>

</body>
</html> -->