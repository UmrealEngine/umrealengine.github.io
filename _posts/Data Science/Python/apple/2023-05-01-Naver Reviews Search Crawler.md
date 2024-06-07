---
layout: single
title: Naver Reviews Search Crawler
tag: Web Crawler
author_profile: false
use_math: false
---

[^]: python 기초 DS

<h3 style="font-size: 8px; margin-top: -45px; font-color: #434343;">
  <a href="https://potettang.github.io/Python/" style="text-decoration: none; color: #3c3c3c; background-color: #f8f9fa; border-radius: 20px; padding: 5px 10px; display: inline-block;">
    <img src="../images/ImgFile/bf.png" style="height: 12.33px; width: auto; margin-top: -4px; vertical-align: middle;" alt="Python 이미지">
    Python / Web crawler & Automation
  </a>
</h3>


<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <style>
        *{margin: 0; padding: 0; box-sizing: border-box;}
        li{list-style: none;}
        a{text-decoration: none; color: inherit;}
        img{vertical-align: top;}
        body {
            margin: 0;
        }
        pheader {
            display: flex;
            justify-content: center;
            align-items: center;
        }
        .img_logo {
            margin-right: 15px;
            max-width: 150px;    
            margin-top: 20px;
        }
        .search_box {
            width: 520px;
            height: 50px;
            border: 2px solid #03cf5d;
            display: flex;
            margin-top: 20px;
        }
        .search_box input {
            width: 90%;
            height: 46px;
            padding-left: 12px;
            padding-right: 12px;
            border: none;
            outline: none;
            font-size: 18px;
        }
        .search_box button {
            width: 10%;
            height: 46px;
            margin: 0;
            padding: 0;
            border: none;
            background: #03cf5d;
        }
        .search_box i {
            color: white;
            font-size: 22px;
            text-align: center;
        }
        #keyboard {
            color: lightgray;
            font-size: 20px;
            text-align: center;
            width: 10%;
            padding-top:12px;
        }
        .card {
            width: 300px;
            height: 450px;
            position: relative;
            perspective: 1000px;
        }
        .card>div{position: absolute; top: 0; left: 0; transition: 2s;}
        .card .front{}
        .card .front img {
            width: 100%;
            height: 100%;
            object-fit: fill;
        }
        .card .back{background: rgba(0, 0, 0, 5); height: 100%; padding: 50px 20px 20px 20px; color: #fff; transform: rotateY(-180deg); backface-visibility: hidden;}
        .card .back h2{margin-bottom: 20px;}
        .card:hover .front{transform: rotateY(180deg);}
        .card:hover .back{transform: rotateY(0)}
        .wrap {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            align-items: center;
            gap: 20px;
            padding: 20px;
        }
        .img_logo {
            margin-right: 15px;
            max-width: 250px;
            margin-top: 20px;
        }
        .loading-spinner {
            position: relative;
            display: flex;
            justify-content: center;
            margin-top: 10px;
        }
        .spinner {
            border: 4px solid rgba(0, 0, 0, 0.1);
            width: 36px;
            height: 36px;
            border-radius: 50%;
            border-left-color: #03cf5d;
            animation: spin 1s linear infinite;
        }
        @keyframes spin {
            0% {
                transform: rotate(0deg);
            }
            100% {
                transform: rotate(360deg);
            }
        }
        </style>
    <script>
        async function fetchData(inputdata) {
            showLoadingSpinner();
            const response = await fetch(`https://api.allorigins.win/get?url=${encodeURIComponent(`https://search.naver.com/search.naver?where=view&sm=tab_jum&query=${inputdata}후기`)}`);
            const { contents } = await response.json();
            const parser = new DOMParser();
            const a = parser.parseFromString(contents, "text/html");
            const b = a.querySelectorAll("a.api_txt_lines");
            const cards = await Promise.all(
                Array.from({ length: Math.min(6, b.length) }, async (_, i) => {
                    const testimage = a.querySelectorAll("img.thumb.api_get")[i];
                    const img_src = testimage.getAttribute("src");
                    const title = b[i].textContent;
                    const url = b[i].getAttribute("href");
                    const card = `
                    <div class="card">
                        <div class="front">
                            <img src="${img_src}">
                        </div>
                        <div class="back">
                            <div class="text">
                                <h2>${title}</h2>
                                <p><a href="${url}" target="_blank">블로그 링크</a></p>
                            </div>
                        </div>
                    </div>
                    `;
                    return card;
                })
            );
            document.querySelector(".wrap").innerHTML = cards.join('');
            hideLoadingSpinner();
        }
        function handleSearch(event) {
            if (event.key === "Enter") {
                fetchData(event.target.value);
            }
        }
        function handleClickSearch() {
            const inputElement = document.querySelector("input[type='text']");
            fetchData(inputElement.value);
        }
        function showLoadingSpinner() {
            const spinner = document.querySelector(".loading-spinner");
            spinner.style.display = "flex";
        }
        function hideLoadingSpinner() {
            const spinner = document.querySelector(".loading-spinner");
            spinner.style.display = "none";
        }
    </script>
</head>
<body>
    <pheader>
        <a href="#"><img
            src="../images/crawer.png"
            class="img_logo" /></a>
        <div class="search_box">
            <input type="text" maxlength="225" onkeypress="handleSearch(event)" placeholder="검색어를 입력하세요.">
            <button onclick="handleClickSearch()">
                <i class="fa fa-search"></i>
            </button>
        </div>
    </pheader>
    <div class="loading-spinner" style="display: none;">
        <div class="spinner"></div>
    </div>
    <div class="search-bar">
        <div class="progress-bar">
            <div class="progress"></div>
        </div>
    </div>
    <div class="wrap"></div>
</body>