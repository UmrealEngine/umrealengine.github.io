---
title: <img src="../images/ImgFile/ppppdf.png" width="200" height="200" referrerpolicy="no-referrer" alt="s1">
permalink: /Python-Syntax1/
layout: single
author_profile: false
sidebar_main: true
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
            .page-divider {
        position: relative;
        width: 100%;
        height: 20px;
        background-color: #FFFDE7;
        z-index: 999;
        }
        /* Add image to the divider */
        .list__item {
            position: relative;
            background-color: #FFFDE7;
            border: none;
            border-radius: 5px;
            padding: 20px;
            margin: 20px auto;
            width: 90%;
            max-width: 800px;
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.18), 0 4px 6px rgba(0, 0, 0, 0.15);
            transition: all 0.3s cubic-bezier(0.25, 0.8, 0.25, 1);
            z-index: 10;
            background-image: linear-gradient(to bottom, rgba(192, 192, 192, 0.2) 1px, transparent 1px);
            background-size: 100% 20px;
        }
        .list__item:before {
            content: '';
            position: absolute;
            left: 76px;
            top: 0;
            bottom: 0;
            width: 3px;
            background-color:#B76E79;
            z-index: -1;
        }
        .list__item:after {
            content: '';
            position: absolute;
            left: 83px;
            top: 0;
            bottom: 0;
            width: 3px;
            background-color: #B76E79;
            z-index: -1;
        }
        .list__item:hover {
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.25), 0 6px 10px rgba(0, 0, 0, 0.22);
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
            font-size: 20px;
            padding: 2px 5px;
        }
        .archive__container {
            max-height: none;
            overflow: hidden;
            transition: max-height 0.3s ease-out;
            overflow: auto;
        }
        .list__item.open .archive__container {
            max-height: none;
            transition: max-height 0.5s ease-in;
        }
        .archive__item {
            padding: 0;
            margin-bottom: 5px;
            clear: both;
            opacity: 1;
            max-height: none;
            overflow: hidden;
            transition: opacity 0.3s ease-out, max-height 0.3s ease-out;
        }
        .archive__item-title {
            font-size: 20px;
            font-weight: 1000;
            margin-bottom: 0;
            padding: 0;
            color: #333;
        }
        .archive__item-title a {
            display: inline;
            color: #3d3d3d;
            text-decoration: none;
            padding: 0;
            margin: 0;
        }
        .archive__item-title a:hover {
            text-decoration: underline;
        }
        .page__meta-date {
            font-size: 14px;
            z-index: 10;
        }
        .page__meta-date {
            font-size: 14px;
            color: #777;
            z-index: 10;
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
            color: #ff5952;
            background-color: rgba(0, 0, 0, 0.1);
        }
        .apple-style .fab {
            font-size: 20px;
            margin-right: 5px;
            vertical-align: middle;
        }
    </style>
</head>

<body>

<div class="list__item">
    <span class="posts-count" style="font-size:12px; font-weight: 500; margin-top: -15px; float: right;">📂 Total 5 post</span>
    <div class="archive__container">
        <div class="archive__item-wrapper">
                <article style="margin-left: 79px" class="archive__item" itemscope="" itemtype="https://schema.org/CreativeWork" data-category="subcategory1">
                    <h3 class="archive__item-title no_toc" itemprop="headline">
                        <a href="https://github.com/99jamsil/StudyArchive/blob/main/Python/Python%20Syntax.md"> 📄 Python syntax complete summary</a>
                                        <p class="page__meta">
                        <span class="page__meta-date">
                            <i class="far fa-calendar-alt" aria-hidden="true"></i>
                            <time datetime="2023-03-15T00:00:00+09:00">2023-03-15</time>
                        </span>
                    </p>
                    </h3>
                </article>
                <article style="margin-left: 79px" class="archive__item" itemscope="" itemtype="https://schema.org/CreativeWork" data-category="subcategory1">
                    <h3 class="archive__item-title no_toc" itemprop="headline">
                        <a href="https://github.com/99jamsil/StudyArchive/blob/main/Python/Python%20Syntax.md"> 📄 Python syntax complete summary</a>
                                        <p class="page__meta">
                        <span class="page__meta-date">
                            <i class="far fa-calendar-alt" aria-hidden="true"></i>
                            <time datetime="2023-03-15T00:00:00+09:00">2023-03-15</time>
                        </span>
                    </p>
                    </h3>
                </article>
                <article style="margin-left: 79px" class="archive__item" itemscope="" itemtype="https://schema.org/CreativeWork" data-category="subcategory1">
                    <h3 class="archive__item-title no_toc" itemprop="headline">
                        <a href="https://github.com/99jamsil/StudyArchive/blob/main/Python/Python%20Syntax.md"> 📄 Python syntax complete summary</a>
                                        <p class="page__meta">
                        <span class="page__meta-date">
                            <i class="far fa-calendar-alt" aria-hidden="true"></i>
                            <time datetime="2023-03-15T00:00:00+09:00">2023-03-15</time>
                        </span>
                    </p>
                    </h3>
                </article>
                <article style="margin-left: 79px" class="archive__item" itemscope="" itemtype="https://schema.org/CreativeWork" data-category="subcategory1">
                    <h3 class="archive__item-title no_toc" itemprop="headline">
                        <a href="https://github.com/99jamsil/StudyArchive/blob/main/Python/Python%20Syntax.md"> 📄 Python syntax complete summary</a>
                                        <p class="page__meta">
                        <span class="page__meta-date">
                            <i class="far fa-calendar-alt" aria-hidden="true"></i>
                            <time datetime="2023-03-15T00:00:00+09:00">2023-03-15</time>
                        </span>
                    </p>
                    </h3>
                </article>
                <article style="margin-left: 79px" class="archive__item" itemscope="" itemtype="https://schema.org/CreativeWork" data-category="subcategory1">
                    <h3 class="archive__item-title no_toc" itemprop="headline">
                        <a href="https://github.com/99jamsil/StudyArchive/blob/main/Python/Python%20Syntax.md"> 📄 Python syntax complete summary</a>
                                        <p class="page__meta">
                        <span class="page__meta-date">
                            <i class="far fa-calendar-alt" aria-hidden="true"></i>
                            <time datetime="2023-03-15T00:00:00+09:00">2023-03-15</time>
                        </span>
                    </p>
                    </h3>
                </article>
                <article style="margin-left: 79px" class="archive__item" itemscope="" itemtype="https://schema.org/CreativeWork" data-category="subcategory1">
                    <h3 class="archive__item-title no_toc" itemprop="headline">
                        <a href="https://github.com/99jamsil/StudyArchive/blob/main/Python/Python%20Syntax.md"> 📄 Python syntax complete summary</a>
                                        <p class="page__meta">
                        <span class="page__meta-date">
                            <i class="far fa-calendar-alt" aria-hidden="true"></i>
                            <time datetime="2023-03-15T00:00:00+09:00">2023-03-15</time>
                        </span>
                    </p>
                    </h3>
                </article>
                <article style="margin-left: 79px" class="archive__item" itemscope="" itemtype="https://schema.org/CreativeWork" data-category="subcategory1">
                    <h3 class="archive__item-title no_toc" itemprop="headline">
                        <a href="https://github.com/99jamsil/StudyArchive/blob/main/Python/Python%20Syntax.md"> 📄 Python syntax complete summary</a>
                                        <p class="page__meta">
                        <span class="page__meta-date">
                            <i class="far fa-calendar-alt" aria-hidden="true"></i>
                            <time datetime="2023-03-15T00:00:00+09:00">2023-03-15</time>
                        </span>
                    </p>
                    </h3>
                </article>
                <article style="margin-left: 79px" class="archive__item" itemscope="" itemtype="https://schema.org/CreativeWork" data-category="subcategory1">
                    <h3 class="archive__item-title no_toc" itemprop="headline">
                        <a href="https://github.com/99jamsil/StudyArchive/blob/main/Python/Python%20Syntax.md"> 📄 Python syntax complete summary</a>
                                        <p class="page__meta">
                        <span class="page__meta-date">
                            <i class="far fa-calendar-alt" aria-hidden="true"></i>
                            <time datetime="2023-03-15T00:00:00+09:00">2023-03-15</time>
                        </span>
                    </p>
                    </h3>
                </article>
                <article style="margin-left: 79px" class="archive__item" itemscope="" itemtype="https://schema.org/CreativeWork" data-category="subcategory1">
                    <h3 class="archive__item-title no_toc" itemprop="headline">
                        <a href="https://github.com/99jamsil/StudyArchive/blob/main/Python/Python%20Syntax.md"> 📄 Python syntax complete summary</a>
                                        <p class="page__meta">
                        <span class="page__meta-date">
                            <i class="far fa-calendar-alt" aria-hidden="true"></i>
                            <time datetime="2023-03-15T00:00:00+09:00">2023-03-15</time>
                        </span>
                    </p>
                    </h3>
                </article>
                <article style="margin-left: 79px" class="archive__item" itemscope="" itemtype="https://schema.org/CreativeWork" data-category="subcategory1">
                    <h3 class="archive__item-title no_toc" itemprop="headline">
                        <a href="https://github.com/99jamsil/StudyArchive/blob/main/Python/Python%20Syntax.md"> 📄 Python syntax complete summary</a>
                                        <p class="page__meta">
                        <span class="page__meta-date">
                            <i class="far fa-calendar-alt" aria-hidden="true"></i>
                            <time datetime="2023-03-15T00:00:00+09:00">2023-03-15</time>
                        </span>
                    </p>
                    </h3>
                </article>
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
        });
    });
</script>
