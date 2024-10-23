---
title: Etc
permalink: /Etc/
layout: single
author_profile: false
sidebar_main: True
---

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
            overflow: auto;
        }
        .list__item.open .archive__container {
            max-height: 500px;
            transition: max-height 0.5s ease-in;
        }
        .archive__item {
            padding: 0;
            margin-bottom: 5px;
            clear: both;
            opacity: 0;
            max-height: 0;
            overflow: hidden;
            transition: opacity 0.3s ease-out, max-height 0.3s ease-out;
        }
        .archive__item-title {
            font-size: 20px;
            font-weight: 600;
            margin-bottom: 0;
            padding: 0;
            color: #333;
        }
        .archive__item-title a {
            display: inline;
            color: #007aff;
            text-decoration: none;
            padding: 0;
            margin: 0;
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
            font-size: 22px;
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
        .subcategory-container {
            display: none;
        }
        .subcategory-container.open {
            display: block;
        }
        .subcategory-text {
            font-size: 12px;
            color: #e6c129;
            margin-left: 3px;
        }
        .apple-style {
            font-family: -apple-system, BlinkMacSystemFont, 'San Francisco', 'Helvetica Neue', Helvetica, Arial, sans-serif;
            font-size: 20px;
            font-weight: 600;
            color: #333;
            letter-spacing: -0.02em;
            text-decoration: none;
            transition: color 0.2s ease-in-out;
            padding: 3px 8px;
            border-radius: 5px;
            background-color: rgba(0, 0, 0, 0.05);
        }
        .apple-style:hover {
            color: #007aff;
            background-color: rgba(0, 0, 0, 0.1);
        }
    </style>

</head>
<body>

<div class="list__item">
    <h2>Programming <span class="posts-count">📂 Total 5 post</span></h2>
    <button class="toggle">View posts</button>   
    <div class="archive__container">
                <div class="archive__item-wrapper">
                <article class="archive__item" itemscope="" itemtype="https://schema.org/CreativeWork" data-category="subcategory1">
                    <h3 class="archive__item-title no_toc" itemprop="headline">
                        <a href="https://github.com/umrealengine/StudyArchive/blob/main/Python/Python%20Syntax.md">총정리</a>
                    </h3>
                </article>
            </div>
        <h3 class="subcategory">Subcategory 1 <span class="subcategory-text">📁2 post</span></h3>
        <div class="subcategory-container">
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
        </div>
        <h3 class="subcategory">Subcategory 2</h3>
        <div class="subcategory-container">
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
        <h3 class="subcategory">Subcategory 3</h3>
        <div class="subcategory-container">
            <!-- 여기에 세부 카테고리 3의 게시물 추가 -->
        </div>
    </div>
</div>


<div class="list__item">
    <h2>Python Syntax <span class="posts-count">📂 Total 5 post</span></h2>
    <button class="toggle">View posts</button>
    <div class="archive__container">
        <h3 class="subcategory">Udemy</h3>
        <div class="subcategory-container">
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
        </div>
        <h3 class="subcategory">Self study</h3>
        <div class="subcategory-container">
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
        <h3 class="subcategory">Subcategory 3</h3>
        <div class="subcategory-container">
            <!-- 여기에 세부 카테고리 3의 게시물 추가 -->
        </div>
    </div>
</div>



<div class="list__item">
    <h2>Algorithm<span class="posts-count">📂 Total 5 post</span></h2>
    <button class="toggle">View posts</button>
    <div class="archive__container">
        <h3 class="subcategory">Udemy</h3>
        <div class="subcategory-container">
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
        </div>
        <h3 class="subcategory">Self study</h3>
        <div class="subcategory-container">
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
        <h3 class="subcategory">Subcategory 3</h3>
        <div class="subcategory-container">
            <!-- 여기에 세부 카테고리 3의 게시물 추가 -->
        </div>
    </div>
</div>

















<script>
    const listItems = document.querySelectorAll('.list__item');
    listItems.forEach(function (listItem) {
        const toggleButton = listItem.querySelector('.toggle');
        toggleButton.addEventListener('click', function () {
            listItem.classList.toggle('open');

            if (!listItem.classList.contains('open')) {
                const openSubcategoryContainers = listItem.querySelectorAll('.subcategory-container.open');
                openSubcategoryContainers.forEach(function (subcategoryContainer) {
                    subcategoryContainer.classList.remove('open');
                });
            }
        });
    });

    const archiveItems = document.querySelectorAll('.archive__item');
    archiveItems.forEach(function (archiveItem) {
        archiveItem.style.transition = 'opacity 0.5s ease-out, max-height 0.5s ease-out';
        archiveItem.style.maxHeight = '0';
        archiveItem.style.opacity = '0';
    });

    const toggleButtons = document.querySelectorAll('.toggle');
    toggleButtons.forEach(function (toggleButton) {
        toggleButton.addEventListener('click', function () {
            const archiveContainer = toggleButton.parentElement.querySelector('.archive__container');
            const archiveItems = archiveContainer.querySelectorAll('.archive__item');

            archiveItems.forEach(function (archiveItem) {
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

    const subcategories = document.querySelectorAll('.subcategory');
    subcategories.forEach(function (subcategory) {
        subcategory.addEventListener('click', function () {
            const subcategoryContainer = subcategory.nextElementSibling;
            subcategoryContainer.classList.toggle('open');

            const siblingSubcategories = subcategory.parentElement.parentElement.querySelectorAll('.subcategory-container');
            siblingSubcategories.forEach(function (siblingSubcategory) {
                if (siblingSubcategory !== subcategoryContainer && siblingSubcategory.classList.contains('open')) {
                    siblingSubcategory.classList.remove('open');
                }
            });
        });
    });
</script>
