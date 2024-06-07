---
title: <img src="../images/ImgFile/Python Logo.png" width="400" height="400" referrerpolicy="no-referrer" alt="s1">
permalink: /naver/
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
        width: 21px;
        height: 21px;
        border-radius: 100%;
        margin-right: 9px;
        box-shadow: 0 1px 2px rgba(0, 0, 0, 0.18), 0 2px 4px rgba(0, 0, 0, 0.15);
    }
    .wrapper {
        display: flex;
        width: 100%;
        height: calc(100vh - 25px);
        margin-top: 25px;
    }
    .content {
        width: 100%;
        padding: 20px 40px 10px;
        overflow-y: auto;
        margin-top: 83px;
        margin-bottom: -1px;
        background-color: #f9fafb;
        border-top-left-radius: 0;
        border-bottom-right-radius: 18px;
        border-left: none;
        border: 0px solid #ffffff;
        box-shadow: 0 6px 8px rgba(0, 0, 0, 0.18), 0 8px 10px rgba(0, 0, 0, 0.15);
        height: calc(100% - 83px);
        box-sizing: border-box;
        border-right: 1px solid #565756;
        border-bottom: 1px solid #565756; 
    }
    .content h3 {
        font-size: 26px;
        font-weight: bold;
        margin-bottom: 5px;
    }
    .content a {
        color: #FFFFFF;
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
        background-color: #03c75a;
        height: 45px;
        padding-left: 10px;
        position: absolute;
        top: 63px;
        width: 100%;
        box-shadow: none;
        box-shadow: 0 -1px 3px rgba(0, 0, 0, 0.18), 0 -2px 4px rgba(0, 0, 0, 0.15);
        border-top-left-radius: 18px;
        border-top-right-radius: 18px;
        border-left: 1px solid #898585;
        border-top: 1px solid #898585; 
        border-right: 1px solid #898585;
    }
</style>

<body>
    <div class="mac-window">
        <div class="circle" style="background-color: #ffffff;"></div>
        <div class="circle" style="background-color: #ffffff;"></div>
        <div class="circle" style="background-color: #ffffff;"></div>
    </div>
    <div class="wrapper">
        <div class="content" id="content"></div>
    </div>
    <script>
        const folders = document.querySelectorAll('.sidebar li');
        const content = document.getElementById('content');
        // Add the "active" class to the first folder
        folders[0].classList.add('active');
        function loadFolderContent(folder) {
            content.innerHTML = '';
            if (folder === 'folder6') {
                content.innerHTML = `
                `;
            } else if (folder === 'folder5') {
                content.innerHTML = `
                `;
            } else if (folder === 'folder4') {
                content.innerHTML = `
                    <h3><a href="https://potettang.github.io/Naver-Reviews-Search-Crawler/"> 📄 Naver Reviews Search Cralwer</a></h3>
                    <p><i class="far fa-calendar-alt"></i><time datetime="2023-03-15T00:00:00+09:00">2023-05-01</time></p>
                    <h3><a href="https://potettang.github.io/Web-Crawler/"> 📄 Web Crawler</a></h3>
                    <p><i class="far fa-calendar-alt"></i><time datetime="2023-03-15T00:00:00+09:00">2023-05-01</time></p>
                    <h3><a href="https://potettang.github.io/Web-Crawler/"> 📄 Web Crawler</a></h3>
                    <p><i class="far fa-calendar-alt"></i><time datetime="2023-03-15T00:00:00+09:00">2023-05-01</time></p>
                `;
            }else if (folder === 'folder3') {
                content.innerHTML = `
                    <h3><a href="https://github.com/potettang/Online-Judge"><i class="fab fa-github"></i> Algorithm Github Link</a></h3>
                `;
            }else if (folder === 'folder2') {
                content.innerHTML = `
                `;
            }else if (folder === 'folder1') {
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
        loadFolderContent('folder6');
    </script>

</body>
