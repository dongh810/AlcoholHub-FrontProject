<script setup>
  import Board from './components/Board.vue';
</script>

<template>
  <header class="header">
    <div class="logo">
            <img src="C:\Users\Playdata\Downloads\AlcoholHub-Front_Project-master\AlcoholHub-Front_Project-master\ahub-project\src\assets\purple.png" class="logoimage">
        </div>
        <div id="menu">
            <ul>
                <li><a href="#">일반 게시판 ▼</a>
                    <ul>
                        <li><a href="#">페어 정보</a></li>
                        <li><a href="#">뉴스 정보</a></li>
                    </ul>
                </li>
                <li><a href="#">정보 게시판 ▼</a>
                    <ul>
                        <li><a href="#">후기 게시판</a></li>
                        <li><a href="#">레시피 공유 게시판</a></li>
                    </ul>
                </li>
            </ul>
        </div>
        <div class="loginbtndiv">
            <button type="button" class="loginbtn" onclick="login()">로그아웃</button>
        </div> 
  </header>

  <Board/>

  <footer class="footer">
    <div class="leftthings">
            <p>
                <span class="ahub">AHUB</span>
                <span>서비스 소개</span>
                <span> | </span>
                <span>서비스 약관</span>
                <span> | </span>
                <span>개인정보 처리방침</span>
                <span> | </span>
                <span>채용</span>
            </p>
        </div>
        <div class="rightthings">
            <p>
                <span>Team Phoenix | 대표: 백동현 | 사업자등록번호:472-56-00332</span><br>
                <span>주소: 서울특별시 동작구 보라매로 87 SFC빌딩 3층</span><br>
                <span>Copyright@2024XI#CIQ ALL RIGHTS RESERVED</span>
            </p>
        </div>
  </footer>

  
</template>

<style scoped>
        /* header css */
  @font-face {
            font-family: 'GmarketSansMedium';
            src: url('https://cdn.jsdelivr.net/gh/projectnoonnu/noonfonts_2001@1.1/GmarketSansMedium.woff') format('woff');
            font-weight: normal;
            font-style: normal;
        }

        * {
            margin: 0;
            padding: 0;
            font-family: 'GmarketSansMedium';
        }

        html, body {
            height: 100%;
            /* background-color: #F1F1F1; */
        }
        
        .header {
            width: 100%;
            height: 100px;
            position: relative;
            top: 0;
            background-color: #F8F9FC;
        }

        .loginbtn {
            background-color: #8c52ff;
            color: white;
            padding: 14px 20px;
            border: none;
            border-radius: 4px;
            cursor: pointer;
            font-size: 16px;
            font-style: bold;
            float: right;
            margin-top: 1.5%;
            margin-right: 2%;
        }
        
        .logoimage {
            width:100px;
        }

        .logo {
            float:left;
            cursor: pointer;
        }

        #menu {
            text-align: center;
            float:left;
            margin-left: 2%;
            margin-top: 2%;
            line-height: 30px; 
            cursor: pointer;
        }

        #menu > ul > li {
            float:left;
            width:140px;
            position:relative;
        }

        #menu > ul > li > ul {
            width:130px;
            display:none;
            position: absolute;
            font-size:14px;
        }

        #menu > ul > li:hover > ul {
            display:block;
        }

        #menu > ul > li > ul > li:hover {
            background: #8c52ff;
            transition: ease 1s;
        }

        ul li {
            list-style: none;
        }

        a {
            text-decoration: none;
            color:#333;
        }

        /* footer css */
        .footer {
            position: relative;
            width: 100%;
            height: 100px;
            background-color: #F8F9FC;
        }

        .rightthings{
            margin-right:50px;
            margin-top:25px;
            float: right;
            font-size: 13px;
        }

        .leftthings{
            margin-left:50px;
            margin-top:45px;
            float: left;
            font-size: 13px;
        }

        .ahub{
            font-size: 15px;
            font-weight: bold;
            margin-right:5px;
        }
</style>
