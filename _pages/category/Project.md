---
title: Project
permalink: /Project/
layout: single
author_profile: false
sidebar_main: true
---
<!-- CSS -->
<style>
  .archive__item {
    display: none; /* 처음에는 article을 숨긴다. */
    margin-bottom: 5px;
  }
  .list__item.open .archive__item {
    display: block; /* list__item에 open 클래스가 있을 때 article을 보이게 한다. */
  }

  .list__item h2 {
    display: inline-block;
    margin-right: 10px;
  }
  .toggle {
    background: none;
    border: none;
    padding: 0;
    margin: 0;
    cursor: pointer;
    font-size: 16px;
  }
  .toggle::before {
    content: "\25BC";
    display: inline-block;
    margin-right: 5px;
  }
  .list__item.open .toggle::before {
    content: "\25B2";
  }
  .archive__item {
    clear: both;
    display: block;
    margin: 0;
    padding: 0;
  }
</style>
<!-- HTML -->
<style>
  .archive__item {
    display: none; /* 처음에는 article을 숨긴다. */
  }
  .list__item.open .archive__item {
    display: block; /* list__item에 open 클래스가 있을 때 article을 보이게 한다. */
  }
  .list__item h2 {
    display: inline-block;
    margin-right: 10px;
  }
  .toggle {
    background: none;
    border: none;
    padding: 0;
    margin: 0;
    cursor: pointer;
    font-size: 16px;
  }
  .toggle::before {
    content: "\25BC";
    display: inline-block;
    margin-right: 5px;
  }
  .list__item.open .toggle::before {
    content: "\25B2";
  }
</style>

<!-- HTML -->
<div class="list__item">
  <h2>ChatGPT API 활용 웹 서비스 <span style="color:red"><font size=2>0 posts</font></span></h2>
  <button class="toggle"></button>
  <article class="archive__item" itemscope="" itemtype="https://schema.org/CreativeWork">
    <h2 class="archive__item-title no_toc" itemprop="headline">
      <a href="/pythonnote/" rel="permalink">python note</a>
    </h2>
    <p class="page__meta">
      <span class="page__meta-date">
        <i class="far fa-calendar-alt" aria-hidden="true"></i>
        <time datetime="2023-02-11T00:00:00+09:00">2023-02-11</time>
      </span>
    </p>
  </article>
  <article class="archive__item" itemscope="" itemtype="https://schema.org/CreativeWork">
    <h2 class="archive__item-title no_toc" itemprop="headline">
      <a href="/pythonnote/" rel="permalink">python note</a>
    </h2>
    <p class="page__meta">
      <span class="page__meta-date">
        <i class="far fa-calendar-alt" aria-hidden="true"></i>
        <time datetime="2023-02-11T00:00:00+09:00">2023-02-11</time>
      </span>
    </p>
  </article>
  <article class="archive__item" itemscope="" itemtype="https://schema.org/CreativeWork">
    <h2 class="archive__item-title no_toc" itemprop="headline">
      <a href="/pythonnote/" rel="permalink">python note</a>
    </h2>
    <p class="page__meta">
      <span class="page__meta-date">
        <i class="far fa-calendar-alt" aria-hidden="true"></i>
        <time datetime="2023-02-11T00:00:00+09:00">2023-02-11</time>
      </span>
    </p>
  </article>
</div>


<div class="list__item">
  <h2>Web service utilizing the ChatGPT API <span style="color:red"><font size=2>0 posts</font></span></h2>
  <button class="toggle"></button>
  <article class="archive__item" itemscope="" itemtype="https://schema.org/CreativeWork">
    <h2 class="archive__item-title no_toc" itemprop="headline">
      <a href="/pythonnote/" rel="permalink">python note</a>
    </h2>
    <p class="page__meta">
      <span class="page__meta-date">
        <i class="far fa-calendar-alt" aria-hidden="true"></i>
        <time datetime="2023-02-11T00:00:00+09:00">2023-02-11</time>
      </span>
    </p>
  </article>
</div>





<!-- JavaScript -->
<script>
  const listItems = document.querySelectorAll('.list__item');
  listItems.forEach(function(listItem) {
    const toggleButton = listItem.querySelector('.toggle');
    toggleButton.addEventListener('click', function() {
      listItem.classList.toggle('open');
      if (listItem.classList.contains('open')) {
        toggleButton.textContent = '';
      } else {
        toggleButton.textContent = '';
      }
    });
  });
</script>