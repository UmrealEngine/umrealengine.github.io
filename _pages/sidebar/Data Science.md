---
title: <img src="../images/ImgFile/Python Logo.png" width="400" height="400" referrerpolicy="no-referrer" alt="s1">
permalink: /Data Science/
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
                <li id="folder5"><img src="../images/ImgFile/d8.png" style="height: 37px; width: auto; margin-top: -4px;" alt="C/C++/C# 이미지"> Fundamentals of Data Science</li>
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
                    <h3><a href="https://potettang.github.io/3E-Pandas-(2)/"> 🚀 게시물 이전 중 🚀</a></h3>
                    <p><i class="far fa-calendar-alt"></i><time datetime="2023-03-15T00:00:00+09:00">2023-09-10</time></p>
                    <h3><span style="color: #42e5e1;">Total 00</span></h3>
                    <h3><span style="background: linear-gradient(to top, #f5be4f 30%, transparent 30%); color: #ffffff;">📂 Python library for Data Analysis, 3E</span></h3>
                    <h3><a href="https://potettang.github.io/3E-Pandas-(2)/"> 📄 [3E 03] Pandas (2)</a></h3>
                    <p><i class="far fa-calendar-alt"></i><time datetime="2023-03-15T00:00:00+09:00">2023-07-06</time></p>
                    <h3><a href="https://potettang.github.io/3E-Pandas-(1)/"> 📄 [3E 02] Pandas (1)</a></h3>
                    <p><i class="far fa-calendar-alt"></i><time datetime="2023-03-15T00:00:00+09:00">2023-07-05</time></p>
                    <h3><a href="https://potettang.github.io/3E-Numpy-(1)/"> 📄 [3E 01] Numpy (1)</a></h3>
                    <p><i class="far fa-calendar-alt"></i><time datetime="2023-03-15T00:00:00+09:00">2023-07-04</time></p>
                    -
                    -
                    <h3><span style="background: linear-gradient(to top, #f5be4f 30%, transparent 30%); color: #ffffff;">📂 Python DataScience</span></h3>
                    <h3><a href="https://potettang.github.io/02;-pandas,-dataframe"> 📄 [02;] Pandas, DataFrame</a></h3>
                    <p><i class="far fa-calendar-alt"></i><time datetime="2023-03-15T00:00:00+09:00">2023-07-03</time></p>
                    <h3><a href="https://potettang.github.io/01;-Numpy"> 📄 [01;] Numpy</a></h3>
                    <p><i class="far fa-calendar-alt"></i><time datetime="2023-03-15T00:00:00+09:00">2023-07-03</time></p>
                    -
                    -
                    <h3><span style="background: linear-gradient(to top, #f5be4f 30%, transparent 30%); color: #ffffff;">📂 Python Syntax (10)</span></h3>
                    <h3><a href="https://potettang.github.io/Python-Syntax-09"> 📄 [Python Syntax 09] 객체지향 프로그래밍</a></h3>
                    <p><i class="far fa-calendar-alt"></i><time datetime="2023-03-15T00:00:00+09:00">2023-07-02</time></p>
                    <h3><a href="https://potettang.github.io/Python-Syntax-08"> 📄 [Python Syntax 08] Function, Module</a></h3>
                    <p><i class="far fa-calendar-alt"></i><time datetime="2023-03-15T00:00:00+09:00">2023-07-02</time></p>
                    <h3><a href="https://potettang.github.io/Python-Syntax-07"> 📄 [Python Syntax 07] 문자열과 내장함수</a></h3>
                    <p><i class="far fa-calendar-alt"></i><time datetime="2023-03-15T00:00:00+09:00">2023-07-02</time></p>
                    <h3><a href="https://potettang.github.io/Python-Syntax-06"> 📄 [Python Syntax 06] dictionary</a></h3>
                    <p><i class="far fa-calendar-alt"></i><time datetime="2023-03-15T00:00:00+09:00">2023-07-01</time></p>               
                    <h3><a href="https://potettang.github.io/Python-Syntax-05"> 📄 [Python Syntax 05] tuple</a></h3>
                    <p><i class="far fa-calendar-alt"></i><time datetime="2023-03-15T00:00:00+09:00">2023-07-01</time></p>                                   
                    <h3><a href="https://potettang.github.io/Python-Syntax-04"> 📄 [Python Syntax 04] list</a></h3>
                    <p><i class="far fa-calendar-alt"></i><time datetime="2023-03-15T00:00:00+09:00">2023-07-01</time></p>
                    <h3><a href="https://potettang.github.io/Python-Syntax-03"> 📄 [Python Syntax 03] 반복문, 조건문</a></h3>
                    <p><i class="far fa-calendar-alt"></i><time datetime="2023-03-15T00:00:00+09:00">2023-07-01</time></p>
                    <h3><a href="https://potettang.github.io/Python-Syntax-02"> 📄 [Python Syntax 02] 연산자</a></h3>
                    <p><i class="far fa-calendar-alt"></i><time datetime="2023-03-15T00:00:00+09:00">2023-07-01</time></p>
                    <h3><a href="https://potettang.github.io/Python-Syntax-01"> 📄 [Python Syntax 01] 변수, 연산자</a></h3>
                    <p><i class="far fa-calendar-alt"></i><time datetime="2023-03-15T00:00:00+09:00">2023-07-01</time></p>
                    -
                    -
                    -
                    <h3><a href="https://github.com/potettang/Online-Judge"><i class="fab fa-github"></i> Algorithm Github Link</a></h3>
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
                    <h3><span style="background: linear-gradient(to top, #f5be4f 30%, transparent 30%); color: #ffffff;">📂 SQLD (10)</span></h3>
                    <h3><a href="https://potettang.github.io/SQLD-10/"> 📄 [SQLD 10] SQL 기본 및 활용-8. PL_SQL</a></h3>
                    <p><i class="far fa-calendar-alt"></i><time datetime="2023-03-15T00:00:00+09:00">2023-06-06</time></p>
                    <h3><a href="https://potettang.github.io/SQLD-9/"> 📄 [SQLD 9] SQL 기본 및 활용-7. Multi-Row Function</a></h3>
                    <p><i class="far fa-calendar-alt"></i><time datetime="2023-03-15T00:00:00+09:00">2023-06-05</time></p>
                    <h3><a href="https://potettang.github.io/SQLD-8/"> 📄 [SQLD 8] SQL 기본 및 활용-6. Subquery</a></h3>
                    <p><i class="far fa-calendar-alt"></i><time datetime="2023-03-15T00:00:00+09:00">2023-06-04</time></p>
                    <h3><a href="https://potettang.github.io/SQLD-7/"> 📄 [SQLD 7]SQL 기본 및 활용-5. Join & Set Operation</a></h3>
                    <p><i class="far fa-calendar-alt"></i><time datetime="2023-03-15T00:00:00+09:00">2023-06-04</time></p>
                    <h3><a href="https://potettang.github.io/SQLD-6/"> 📄 [SQLD 6] SQL 기본 및 활용 -4. TCL & DCL</a></h3>
                    <p><i class="far fa-calendar-alt"></i><time datetime="2023-03-15T00:00:00+09:00">2023-06-03</time></p>
                    <h3><a href="https://potettang.github.io/SQLD-5/"> 📄 [SQLD 5] SQL 기본 및 활용 -3. Function</a></h3>
                    <p><i class="far fa-calendar-alt"></i><time datetime="2023-03-15T00:00:00+09:00">2023-06-03</time></p>
                    <h3><a href="https://potettang.github.io/SQLD-4/"> 📄 [SQLD 4] SQL 기본 및 활용 -2. DDL</a></h3>
                    <p><i class="far fa-calendar-alt"></i><time datetime="2023-03-15T00:00:00+09:00">2023-06-02</time></p>
                    <h3><a href="https://potettang.github.io/SQLD-3/"> 📄 [SQLD 3] SQL 기본 및 활용 -1. Basic DML</a></h3>
                    <p><i class="far fa-calendar-alt"></i><time datetime="2023-03-15T00:00:00+09:00">2023-06-02</time></p>
                    <h3><a href="https://potettang.github.io/SQLD-2/"> 📄 [SQLD 2] 데이터 모델과 성능</a></h3>
                    <p><i class="far fa-calendar-alt"></i><time datetime="2023-03-15T00:00:00+09:00">2023-06-01</time></p>
                    <h3><a href="https://potettang.github.io/SQLD-1/"> 📄 [SQLD 1] 데이터 모델링의 이해</a></h3>
                    <p><i class="far fa-calendar-alt"></i><time datetime="2023-03-15T00:00:00+09:00">2023-06-01</time></p>
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
