---
title: <img src="../images/ImgFile/Python Logo.png" width="250" height="200" referrerpolicy="no-referrer" alt="s1">
permalink: /test1/
layout: single
author_profile: false
sidebar_main: true
---
<style>
    * {
        box-sizing: border-box;
    }
    body {
        font-family: 'San Francisco', 'Helvetica Neue', Helvetica, Arial, sans-serif;
        margin: 0;
        padding: 0;
    }
    .circle {
        width: 12px;
        height: 12px;
        border-radius: 50%;
        margin-right: 5px;
        box-shadow: 0 1px 2px rgba(0, 0, 0, 0.18), 0 2px 4px rgba(0, 0, 0, 0.15);
    }
    .wrapper {
        display: flex;
        width: 100%;
        height: calc(100vh - 25px);
        margin-top: 25px;
    }
    .sidebar {
        background-color: #282828;
        width: 33%;
        padding: 20px;
        border-top-right-radius: 0;
        border-bottom-left-radius: 12px;
        border-right: none;
        margin-top: 83px;
        border: 0px solid #57606a;
        box-shadow: 0 6px 8px rgba(0, 0, 0, 0.18), 0 8px 10px rgba(0, 0, 0, 0.15);
        height: calc(100% - 83px);
        overflow-y: auto;
        box-sizing: border-box;
    }
    .sidebar h2 {
        font-size: 30px;
        margin-bottom: 20px;
        color: #c9d1d9;
    }
    .sidebar ul {
        list-style-type: none;
        padding: 0;
    }
    .sidebar li {
        padding: 10px 0;
        cursor: pointer;
        color: #c9d1d9;
        position: relative;
        font-size: 20px; /* 원하는 글자 크기로 조절하세요 */
        font-weight: bold;
    }
    .sidebar li::after {
        content: "";
        position: absolute;
        bottom: 0;
        left: 0;
        right: 0;
        height: 2px;
        transform: scaleX(0);
        transform-origin: left;
        transition: transform 0.3s;
    }
    .sidebar li.active {
        color: #ff0080;
    }
    .sidebar li.active::after {
        transform: scaleX(1);
    }
    .sidebar li:hover::after {
        transform: scaleX(0);
    }
    .content {
        width: 70%;
        padding: 20px 40px 10px;
        overflow-y: auto;
        margin-top: 83px;
        margin-left: -1px;
        margin-bottom: -1px;
        background-color: #f7f7f8;
        border-top-left-radius: 0;
        border-bottom-right-radius: 12px;
        border-left: none;
        border: 0px solid #57606a;
        box-shadow: 0 6px 8px rgba(0, 0, 0, 0.18), 0 8px 10px rgba(0, 0, 0, 0.15);
        height: calc(100% - 83px);
        box-sizing: border-box;
    }
    .content h3 {
        font-size: 22px;
        font-weight: bold;
        margin-bottom: 5px;
    }
    .content a {
        color: #333;
        text-decoration: none;
    }
    .content a:hover {
        text-decoration: underline;
    }
    .content p {
        font-size: 16px;
        color: #777;
        margin: 0 0 20px;
    }
    .content i {
        margin-right: 5px;
    }
    .mac-window {
        display: flex;
        justify-content: flex-start;
        align-items: center;
        background-color: #57606a;
        height: 25px;
        padding-left: 10px;
        position: absolute;
        top: 83px;
        width: 99.9%;
        box-shadow: none;
        box-shadow: 0 -1px 3px rgba(0, 0, 0, 0.18), 0 -2px 4px rgba(0, 0, 0, 0.15);
        border-top-left-radius: 12px;
        border-top-right-radius: 12px;
    }
</style>

<body>
    <div class="mac-window">
        <div class="circle" style="background-color: #afb8c1;"></div>
        <div class="circle" style="background-color: #afb8c1;"></div>
        <div class="circle" style="background-color: #afb8c1;"></div>
    </div>
    <div class="wrapper">
        <div class="sidebar">
            <h2>Python</h2>
            <ul>
                <li id="folder3">Algorithm</li>
                <li id="folder2">Web crawler / Automation</li>
                <li id="folder1">Learning Python by Yourself</li>
            </ul>
        </div>
        <div class="content" id="content"></div>
    </div>
    <script>
        const folders = document.querySelectorAll('.sidebar li');
        const content = document.getElementById('content');
        // Add the "active" class to the first folder
        folders[0].classList.add('active');
        function loadFolderContent(folder) {
            content.innerHTML = '';
            if (folder === 'folder3') {
                content.innerHTML = `
                    <h3><a href="https://github.com/potettang/StudyArchive/blob/main/Python/Python%20Syntax.md"><i class="fab fa-github"></i> Algorithm Github Link</a></h3>
                `;
            } else if (folder === 'folder2') {
                content.innerHTML = `
                    <h3><a href="https://potettang.github.io/Naver-Reviews-Search-Crawler/"> 📄 Naver Reviews Search Cralwer</a></h3>
                    <p><i class="far fa-calendar-alt"></i><time datetime="2023-03-15T00:00:00+09:00">2023-05-01</time></p>
                    <h3><a href="https://potettang.github.io/Web-Crawler/"> 📄 Web Crawler</a></h3>
                    <p><i class="far fa-calendar-alt"></i><time datetime="2023-03-15T00:00:00+09:00">2023-05-01</time></p>
                `;
            } else if (folder === 'folder1') {
                content.innerHTML = `
                `;
            }
        }
        folders.forEach(folder => {
            folder.addEventListener('click', () => {
                // Remove the "active" class from all the folders
                folders.forEach(f => f.classList.remove('active'));
                const folderId = folder.getAttribute('id');
                // Add the "active" class to the clicked folder
                folder.classList.add('active');
                loadFolderContent(folderId);
            });
        });
        // Load the first folder by default
        loadFolderContent('folder3');
    </script>

</body>
