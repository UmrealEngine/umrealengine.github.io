---
title: 
permalink: /UnrealEngine/
layout: single
author_profile: false
sidebar_main: false
---


<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <style>
        * {
            box-sizing: border-box;
        }
        body {
            font-family: 'San Francisco', 'Helvetica Neue', Helvetica, Arial, sans-serif;
            margin: 0;
            padding: 0;
        }
        .circle1 {
            width: 21px;
            height: 21px;
            border-radius: 100%;
            margin-right: 9px;
            box-shadow: 0 1px 2px rgba(0, 0, 0, 0.18), 0 2px 4px rgba(0, 0, 0, 0.15);
        }
        .circle1:hover {
            box-shadow: 0 1px 2px rgba(0, 0, 0, 0.18), 0 2px 4px rgba(0, 0, 0, 0.15), 0 0 10px #ec695e;
            transition: box-shadow 0.3s ease;
        }
        .circle2 {
            width: 21px;
            height: 21px;
            border-radius: 100%;
            margin-right: 9px;
            box-shadow: 0 1px 2px rgba(0, 0, 0, 0.18), 0 2px 4px rgba(0, 0, 0, 0.15);
        }
        .circle2:hover {
            box-shadow: 0 1px 2px rgba(0, 0, 0, 0.18), 0 2px 4px rgba(0, 0, 0, 0.15), 0 0 10px #f5be4f;
            transition: box-shadow 0.3s ease;
        }
        .circle3 {
            width: 21px;
            height: 21px;
            border-radius: 100%;
            margin-right: 9px;
            box-shadow: 0 1px 2px rgba(0, 0, 0, 0.18), 0 2px 4px rgba(0, 0, 0, 0.15);
        }
        .circle3:hover {
            box-shadow: 0 1px 2px rgba(0, 0, 0, 0.18), 0 2px 4px rgba(0, 0, 0, 0.15), 0 0 10px #61c455;
            transition: box-shadow 0.3s ease;
        }
        .wrapper {
            display: flex;
            width: 100%;
            height: 640px;
            margin-top: 25px;
            padding-top: 63px;
        }
        .sidebar-wrapper {
            position: relative;
            width: 250px;
        }
        .mac-window {
            display: flex;
            justify-content: flex-start;
            align-items: center;
            background-color: #1e1e1e;
            height: 45px;
            padding-left: 10px;
            position: absolute;
            top: 0;
            width: 100%;
            box-shadow: none;
            box-shadow: 0 -1px 3px rgba(0, 0, 0, 0.18), 0 -2px 4px rgba(0, 0, 0, 0.15);
            border-top-left-radius: 18px;
            border-top-right-radius: 18px;
            border-left: 1px solid #898585;
            border-top: 1px solid #898585;
            border-right: 1px solid #898585;
            overflow: hidden; /* 추가: mac-window 내 요소들이 넘치지 않도록 설정 */
        }
            .mac-window .current-page {
                font-size: 15px; /* 사이드바 글자 크기와 일치 */
                color: #5f5f5f; /* 사이드바 글자 색상과 일치 */
                font-weight: bold; /* 사이드바 글자 두께와 일치 */
                margin-left: auto; /* 왼쪽의 다른 요소들과의 간격을 유지하고 오른쪽 정렬 */
                margin-right: 20px; /* 오른쪽 여백 추가 */
                white-space: nowrap; /* 추가: 텍스트가 한 줄로 유지되도록 설정 */
                overflow: hidden; /* 추가: 넘치는 텍스트를 숨김 */
                text-overflow: ellipsis; /* 추가: 넘치는 텍스트가 ...으로 표시되도록 설정 */
            }
        .sidebar {
            background-color: #282828;
            border-top-right-radius: 0;
            border-bottom-left-radius: 18px;
            border-bottom-right-radius: 18px;
            border-right: none;
            margin-top: -43px;
            border: 0px solid #57606a;
            box-shadow: 0 6px 8px rgba(0, 0, 0, 0.18), 0 8px 10px rgba(0, 0, 0, 0.15);
            height: 600px;
            overflow-y: auto;
            box-sizing: border-box;
            border-left: 1px solid #565756;
            border-bottom: 1px solid #565756;
            width: 100%;
            position: static;
        }
        .sidebar h2 {
            font-size: 30px;
            margin-bottom: 20px;
            color: white;
        }
        .sidebar ul {
            list-style-type: none;
            padding: 10px;
            display: flex;
            flex-wrap: wrap;
            flex-direction: row;
            justify-content: flex-start;
        }
        .sidebar li {
            padding: 10px;
            cursor: pointer;
            color: #5f5f5f;
            position: relative;
            font-size: 20px;
            font-weight: bold;
            flex: 0 0 calc(25% - 10px);
            box-sizing: border-box;
            margin-bottom: 40px;
        }
        .sidebar li::after {
            content: ""; /* 변경된 부분: 줄 제거 */
            position: absolute;
            bottom: 0;
            left: 0;
            right: 0;
            height: 2px;    
            background-color: transparent; /* 변경된 부분: 줄 제거 */
            transform: scaleX(0);
            transform-origin: left;
            transition: transform 0.3s;
        }
        .sidebar li:hover {
            color: #42e5e1; /* 변경된 부분: 텍스트 색상 변경 */
        }
        .sidebar li.active::after,
        .sidebar li:hover::after {
            transform: scaleX(1);
        }
        .image-text-container {
            display: flex;
            flex-direction: column;
            align-items: center;
            text-align: flex-start;
        }
        .input {
            margin: 30px;
            background: none;
            border: none;
            outline: none;
            max-width: 150px;
            padding: 10px 20px;
            font-size: 16px;
            color: #fff;
        }
        .sidebar li a {
            text-decoration: none;
            color: inherit;
        }
        .sidebar li a:hover {
            color: inherit;
        }
        /* tool tip_start*/
        ul {
        list-style: none;
        }
        .example-2 {
        display: flex;
        justify-content: center;
        align-items: center;
        }
        .example-2 .icon-content {
        margin: 0 10px;
        position: relative;
        }
        .example-2 .icon-content .tooltip {
        position: absolute;
        top: -30px;
        left: 50%;
        transform: translateX(-50%);
        color: #fff;
        padding: 6px 10px;
        border-radius: 5px;
        opacity: 0;
        visibility: hidden;
        font-size: 14px;
        transition: all 0.3s ease;
        }
        .example-2 .icon-content:hover .tooltip {
        opacity: 1;
        visibility: visible;
        top: -50px;
        }
        .example-2 .icon-content a {
        position: relative;
        overflow: hidden;
        display: flex;
        justify-content: center;
        align-items: center;
        width: 50px;
        height: 50px;
        border-radius: 50%;
        color: #4d4d4d;
        background-color: #fff;
        transition: all 0.3s ease-in-out;
        }
        .example-2 .icon-content a:hover {
        box-shadow: 3px 2px 45px 0px rgb(0 0 0 / 12%);
        }
        .example-2 .icon-content a svg {
        position: relative;
        z-index: 1;
        width: 30px;
        height: 30px;
        }
        .example-2 .icon-content a:hover {
        color: white;
        }
        .example-2 .icon-content a .filled {
        position: absolute;
        top: auto;
        bottom: 0;
        left: 0;
        width: 100%;
        height: 0;
        background-color: #000;
        transition: all 0.3s ease-in-out;
        }
        .example-2 .icon-content a:hover .filled {
        height: 100%;
        }
        .example-2 .icon-content a[data-social="linkedin"] .filled,
        .example-2 .icon-content a[data-social="linkedin"] ~ .tooltip {
        background-color: #0274b3;
        }
        .example-2 .icon-content a[data-social="github"] .filled,
        .example-2 .icon-content a[data-social="github"] ~ .tooltip {
        background-color: #24262a;
        }
        .example-2 .icon-content a[data-social="instagram"] .filled,
        .example-2 .icon-content a[data-social="instagram"] ~ .tooltip {
        background: linear-gradient(
            45deg,
            #405de6,
            #5b51db,
            #b33ab4,
            #c135b4,
            #e1306c,
            #fd1f1f
        );
        }
        .example-2 .icon-content a[data-social="youtube"] .filled,
        .example-2 .icon-content a[data-social="youtube"] ~ .tooltip {
        background-color: #ff0000;
        }
        /* tool tip_end*/
        .example-3 {
        display: flex;
        justify-content: center;
        align-items: center;
        }
        .example-3 .icon-content {
        margin: 0 10px;
        position: relative;
        }
        .example-3 .icon-content .tooltip {
        position: absolute;
        top: -30px;
        left: 50%;
        transform: translateX(-50%);
        color: #fff;
        padding: 6px 10px;
        border-radius: 5px;
        opacity: 0;
        visibility: hidden;
        font-size: 14px;
        transition: all 0.3s ease;
        }
        .example-3 .icon-content:hover .tooltip {
        opacity: 1;
        visibility: visible;
        top: -50px;
        }
        .example-3 .icon-content a {
        position: relative;
        overflow: hidden;
        display: flex;
        justify-content: center;
        align-items: center;
        width: 50px;
        height: 50px;
        border-radius: 50%;
        color: #4d4d4d;
        background-color: #fff;
        transition: all 0.3s ease-in-out;
        }
        .example-3 .icon-content a:hover {
        box-shadow: 3px 2px 45px 0px rgb(0 0 0 / 12%);
        }
        .example-3 .icon-content a svg {
        position: relative;
        z-index: 1;
        width: 30px;
        height: 30px;
        }
        .example-3 .icon-content a:hover {
        color: white;
        }
        .example-3 .icon-content a .filled {
        position: absolute;
        top: auto;
        bottom: 0;
        left: 0;
        width: 100%;
        height: 0;
        background-color: #000;
        transition: all 0.3s ease-in-out;
        }
        .example-3 .icon-content a:hover .filled {
        height: 100%;
        }
        .example-3 .icon-content a[data-social="discord"] .filled,
        .example-3 .icon-content a[data-social="discord"] ~ .tooltip {
        background-color: #7289da;
        }
        .example-3 .icon-content a[data-social="steam"] .filled,
        .example-3 .icon-content a[data-social="steam"] ~ .tooltip {
        background-color: #171d25;
        }
        .example-3 .icon-content a[data-social="instagram"] .filled,
        .example-3 .icon-content a[data-social="instagram"] ~ .tooltip {
        background: linear-gradient(
            45deg,
            #405de6,
            #5b51db,
            #b33ab4,
            #c135b4,
            #e1306c,
            #fd1f1f
        );
        }
        .example-3 .icon-content a[data-social="youtube"] .filled,
        .example-3 .icon-content a[data-social="youtube"] ~ .tooltip {
        background-color: #ff0000;
        }
    </style>
</head>

<body>
    <div class="mac-window">
        <div class="circle1" style="background-color: #ec695e;"></div>
        <div class="circle2" style="background-color: #f5be4f;"></div>
        <div class="circle3" style="background-color: #424242;"></div>
        <input placeholder="Search" class="input" name="text" type="text">
        <span class="current-page">↳ <img src="../images/ImgFile/mainfolder/blue.png" style="height: 15px; width: auto; margin-top: -4px;" alt=""> Unreal Engine</span>
    </div>
    <div class="wrapper">
        <div class="sidebar">
            <ul>
                <li id="folder1">
                    <a href="https://potettang.github.io/MetaverseAcademy/" class="image-text-container">
                        <img src="../images/ImgFile/mainfolder/blue.png" style="height: 37px; width: auto; margin-top: -4px;" alt="">
                        <span>Metaverse Academy</span>
                    </a>
                </li>
                <li id="folder1">
                    <a href="https://potettang.github.io/UnrealEngine_UEC++Developer/" class="image-text-container">
                        <img src="../images/ImgFile/mainfolder/blue.png" style="height: 37px; width: auto; margin-top: -4px;" alt="">
                        <span>UE5_C++ Developer</span>
                    </a>
                </li>
            </ul>
        </div>
        <div class="content" id="content"></div>
    </div>
    <script>
        const folders = document.querySelectorAll('.sidebar li');
        const content = document.getElementById('content');
        const input = document.querySelector('.input');
        const sidebarUl = document.querySelector('.sidebar ul');
        // Add the "active" class to the first folder
        folders[0].classList.add('active');
        function loadFolderContent(folder) {
            content.innerHTML = '';
        }
        folders.forEach(folder => {
            // 이벤트 리스너를 추가합니다.
            folder.addEventListener('click', () => {
                // Remove the "active" class from all the folders
                folders.forEach(f => f.classList.remove('active'));
                const folderId = folder.getAttribute('id');
                // Add the "active" class to the clicked folder
                folder.classList.add('active');
                loadFolderContent(folderId);
            });
            // 이벤트 리스너를 추가하여 마우스가 요소 위에 있을 때 "active" 클래스를 추가합니다.
            folder.addEventListener('mouseover', () => {
                folder.classList.add('active');
            });
            // 마우스가 요소 위에서 벗어날 때 "active" 클래스를 제거합니다.
            folder.addEventListener('mouseout', () => {
                folder.classList.remove('active');
            });
        });
        // Load the first folder by default
        loadFolderContent('folder1');
        input.addEventListener('input', function () {
            const searchText = input.value.toLowerCase();
            folders.forEach(folder => {
                const spanText = folder.querySelector('span').textContent.toLowerCase();
                if (spanText.includes(searchText)) {
                    folder.style.display = 'block';
                } else {
                    folder.style.display = 'none';
                }
            });
        });
        document.addEventListener('DOMContentLoaded', function () {
            var circle = document.querySelector('.circle1');
            circle.addEventListener('click', function () {
                window.location.href = 'https://potettang.github.io/main/';
            });
        });
        var circle2 = document.querySelector('.circle2');
        circle2.addEventListener('click', function () {
            history.back();
        });
        var circle3 = document.querySelector('.circle3');
        circle3.addEventListener('click', function () {
            history.forward();
        });
    </script>
</body>


<ul class="example-2">
  <li class="icon-content">
    <a href="https://discord.gg/ZM2ZWHJSUW" aria-label="Discord" data-social="discord">
      <div class="filled"></div>
      <svg
        viewBox="0 0 16 16"
        class="bi bi-discord"
        fill="currentColor"
        height="16"
        width="16"
        xmlns="http://www.w3.org/2000/svg"
      >
        <path
          d="M13.545 2.907a13.2 13.2 0 0 0-3.257-1.011.05.05 0 0 0-.052.025c-.141.25-.297.577-.406.833a12.2 12.2 0 0 0-3.658 0 8 8 0 0 0-.412-.833.05.05 0 0 0-.052-.025c-1.125.194-2.22.534-3.257 1.011a.04.04 0 0 0-.021.018C.356 6.024-.213 9.047.066 12.032q.003.022.021.037a13.3 13.3 0 0 0 3.995 2.02.05.05 0 0 0 .056-.019q.463-.63.818-1.329a.05.05 0 0 0-.01-.059l-.018-.011a9 9 0 0 1-1.248-.595.05.05 0 0 1-.02-.066l.015-.019q.127-.095.248-.195a.05.05 0 0 1 .051-.007c2.619 1.196 5.454 1.196 8.041 0a.05.05 0 0 1 .053.007q.121.1.248.195a.05.05 0 0 1-.004.085 8 8 0 0 1-1.249.594.05.05 0 0 0-.03.03.05.05 0 0 0 .003.041c.24.465.515.909.817 1.329a.05.05 0 0 0 .056.019 13.2 13.2 0 0 0 4.001-2.02.05.05 0 0 0 .021-.037c.334-3.451-.559-6.449-2.366-9.106a.03.03 0 0 0-.02-.019m-8.198 7.307c-.789 0-1.438-.724-1.438-1.612s.637-1.613 1.438-1.613c.807 0 1.45.73 1.438 1.613 0 .888-.637 1.612-1.438 1.612m5.316 0c-.788 0-1.438-.724-1.438-1.612s.637-1.613 1.438-1.613c.807 0 1.451.73 1.438 1.613 0 .888-.631 1.612-1.438 1.612"
        ></path>
      </svg>
    </a>
    <div class="tooltip">Discord</div>
  </li>
  <li class="icon-content">
    <a
      href="https://github.com/potettang"
      aria-label="LinkedIn"
      data-social="linkedin"
    >
      <div class="filled"></div>
      <svg
        xmlns="http://www.w3.org/2000/svg"
        width="16"
        height="16"
        fill="currentColor"
        class="bi bi-linkedin"
        viewBox="0 0 16 16"
        xml:space="preserve"
      >
        <path
          d="M0 1.146C0 .513.526 0 1.175 0h13.65C15.474 0 16 .513 16 1.146v13.708c0 .633-.526 1.146-1.175 1.146H1.175C.526 16 0 15.487 0 14.854zm4.943 12.248V6.169H2.542v7.225zm-1.2-8.212c.837 0 1.358-.554 1.358-1.248-.015-.709-.52-1.248-1.342-1.248S2.4 3.226 2.4 3.934c0 .694.521 1.248 1.327 1.248zm4.908 8.212V9.359c0-.216.016-.432.08-.586.173-.431.568-.878 1.232-.878.869 0 1.216.662 1.216 1.634v3.865h2.401V9.25c0-2.22-1.184-3.252-2.764-3.252-1.274 0-1.845.7-2.165 1.193v.025h-.016l.016-.025V6.169h-2.4c.03.678 0 7.225 0 7.225z"
          fill="currentColor"
        ></path>
      </svg>
    </a>
  </li>
  <li class="icon-content">
    <a href="https://github.com/potettang" aria-label="GitHub" data-social="github">
      <div class="filled"></div>
      <svg
        xmlns="http://www.w3.org/2000/svg"
        width="16"
        height="16"
        fill="currentColor"
        class="bi bi-github"
        viewBox="0 0 16 16"
        xml:space="preserve"
      >
        <path
          d="M8 0C3.58 0 0 3.58 0 8c0 3.54 2.29 6.53 5.47 7.59.4.07.55-.17.55-.38 0-.19-.01-.82-.01-1.49-2.01.37-2.53-.49-2.69-.94-.09-.23-.48-.94-.82-1.13-.28-.15-.68-.52-.01-.53.63-.01 1.08.58 1.23.82.72 1.21 1.87.87 2.33.66.07-.52.28-.87.51-1.07-1.78-.2-3.64-.89-3.64-3.95 0-.87.31-1.59.82-2.15-.08-.2-.36-1.02.08-2.12 0 0 .67-.21 2.2.82.64-.18 1.32-.27 2-.27s1.36.09 2 .27c1.53-1.04 2.2-.82 2.2-.82.44 1.1.16 1.92.08 2.12.51.56.82 1.27.82 2.15 0 3.07-1.87 3.75-3.65 3.95.29.25.54.73.54 1.48 0 1.07-.01 1.93-.01 2.2 0 .21.15.46.55.38A8.01 8.01 0 0 0 16 8c0-4.42-3.58-8-8-8"
          fill="currentColor"
        ></path>
      </svg>
    </a>
  </li>
  <li class="icon-content">
    <a
      href="https://github.com/potettang"
      aria-label="Instagram"
      data-social="instagram"
    >
      <div class="filled"></div>
      <svg
        xmlns="http://www.w3.org/2000/svg"
        width="16"
        height="16"
        fill="currentColor"
        class="bi bi-instagram"
        viewBox="0 0 16 16"
        xml:space="preserve"
      >
        <path
          d="M8 0C5.829 0 5.556.01 4.703.048 3.85.088 3.269.222 2.76.42a3.9 3.9 0 0 0-1.417.923A3.9 3.9 0 0 0 .42 2.76C.222 3.268.087 3.85.048 4.7.01 5.555 0 5.827 0 8.001c0 2.172.01 2.444.048 3.297.04.852.174 1.433.372 1.942.205.526.478.972.923 1.417.444.445.89.719 1.416.923.51.198 1.09.333 1.942.372C5.555 15.99 5.827 16 8 16s2.444-.01 3.298-.048c.851-.04 1.434-.174 1.943-.372a3.9 3.9 0 0 0 1.416-.923c.445-.445.718-.891.923-1.417.197-.509.332-1.09.372-1.942C15.99 10.445 16 10.173 16 8s-.01-2.445-.048-3.299c-.04-.851-.175-1.433-.372-1.941a3.9 3.9 0 0 0-.923-1.417A3.9 3.9 0 0 0 13.24.42c-.51-.198-1.092-.333-1.943-.372C10.443.01 10.172 0 7.998 0zm-.717 1.442h.718c2.136 0 2.389.007 3.232.046.78.035 1.204.166 1.486.275.373.145.64.319.92.599s.453.546.598.92c.11.281.24.705.275 1.485.039.843.047 1.096.047 3.231s-.008 2.389-.047 3.232c-.035.78-.166 1.203-.275 1.485a2.5 2.5 0 0 1-.599.919c-.28.28-.546.453-.92.598-.28.11-.704.24-1.485.276-.843.038-1.096.047-3.232.047s-2.39-.009-3.233-.047c-.78-.036-1.203-.166-1.485-.276a2.5 2.5 0 0 1-.92-.598 2.5 2.5 0 0 1-.6-.92c-.109-.281-.24-.705-.275-1.485-.038-.843-.046-1.096-.046-3.233s.008-2.388.046-3.231c.036-.78.166-1.204.276-1.486.145-.373.319-.64.599-.92s.546-.453.92-.598c.282-.11.705-.24 1.485-.276.738-.034 1.024-.044 2.515-.045zm4.988 1.328a.96.96 0 1 0 0 1.92.96.96 0 0 0 0-1.92m-4.27 1.122a4.109 4.109 0 1 0 0 8.217 4.109 4.109 0 0 0 0-8.217m0 1.441a2.667 2.667 0 1 1 0 5.334 2.667 2.667 0 0 1 0-5.334"
          fill="currentColor"
        ></path>
      </svg>
    </a>
  </li>
  <li class="icon-content">
    <a href="https://youtube.com/@potettang?si=wYfVSBnx9RfnGoCo" aria-label="Youtube" data-social="youtube">
      <div class="filled"></div>
      <svg
        xmlns="http://www.w3.org/2000/svg"
        width="16"
        height="16"
        fill="currentColor"
        class="bi bi-youtube"
        viewBox="0 0 16 16"
        xml:space="preserve"
      >
        <path
          d="M8.051 1.999h.089c.822.003 4.987.033 6.11.335a2.01 2.01 0 0 1 1.415 1.42c.101.38.172.883.22 1.402l.01.104.022.26.008.104c.065.914.073 1.77.074 1.957v.075c-.001.194-.01 1.108-.082 2.06l-.008.105-.009.104c-.05.572-.124 1.14-.235 1.558a2.01 2.01 0 0 1-1.415 1.42c-1.16.312-5.569.334-6.18.335h-.142c-.309 0-1.587-.006-2.927-.052l-.17-.006-.087-.004-.171-.007-.171-.007c-1.11-.049-2.167-.128-2.654-.26a2.01 2.01 0 0 1-1.415-1.419c-.111-.417-.185-.986-.235-1.558L.09 9.82l-.008-.104A31 31 0 0 1 0 7.68v-.123c.002-.215.01-.958.064-1.778l.007-.103.003-.052.008-.104.022-.26.01-.104c.048-.519.119-1.023.22-1.402a2.01 2.01 0 0 1 1.415-1.42c.487-.13 1.544-.21 2.654-.26l.17-.007.172-.006.086-.003.171-.007A100 100 0 0 1 7.858 2zM6.4 5.209v4.818l4.157-2.408z"
          fill="currentColor"
        ></path>
      </svg>
    </a>
  </li>
</ul>