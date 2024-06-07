---
title: "Medical AI"
permalink: /Medical AI/
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
    .sidebar {
        background-color: #282828;
        width: 41%;
        padding: 20px;
        border-top-right-radius: 0;
        border-bottom-left-radius: 18px;
        border-right: none;
        margin-top: 83px;
        border: 0px solid #57606a;
        box-shadow: 0 6px 8px rgba(0, 0, 0, 0.18), 0 8px 10px rgba(0, 0, 0, 0.15);
        height: calc(100% - 83px);
        overflow-y: auto;
        box-sizing: border-box;
        border-left: 1px solid #565756;
        border-bottom: 1px solid #565756; 
    }
    .sidebar h2 {
        font-size: 30px;
        margin-bottom: 20px;
        color: white;
    }
    .sidebar ul {
        list-style-type: none;
        padding: 0;
    }
    .sidebar li {
        padding: 10px 0;
        cursor: pointer;
        color: #5f5f5f;
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
        color: #42e5e1;
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
        background-color: #000000;
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
        background-color: #1e1e1e;
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
        <div class="circle" style="background-color: #ec695e;"></div>
        <div class="circle" style="background-color: #f5be4f;"></div>
        <div class="circle" style="background-color: #424242;"></div>
    </div>
    <div class="wrapper">
        <div class="sidebar">
            <ul>
                <li id="folder5"><img src="../images/ImgFile/d8.png" style="height: 37px; width: auto; margin-top: -4px;" alt="C/C++/C# 이미지"> Medical Data Preprocessing and Processing</li>
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
            if (folder === 'folder5') {
                content.innerHTML = `
                `;
            } else if (folder === 'folder4') {
                content.innerHTML = `
                `;
            } else if (folder === 'folder3') {
                content.innerHTML = `
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
        loadFolderContent('folder5');
    </script>

</body>
<br/>
<img src="../images/ImgFile/Medicalbottomimg.jpg" width="100%" height="1000" referrerpolicy="no-referrer" alt="s1" style="border-radius:20px;">