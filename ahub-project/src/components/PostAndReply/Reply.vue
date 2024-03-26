<template>
    <div class="replytitlediv">
        <h2 class="replytitle">댓글</h2>
    </div>
    <hr class="replyline">
    <div class="replywriterdiv">
        <p>포도나무지기</p>
    </div>
    <div class="replycontentdiv">
        <p>
            와 정말 맛있겠네요, 저도 이번 주말에 도전해봐야 할것 같습니다!
        </p>
    </div>
    <div class="replydatediv">
        <p>2024.03.16 10:29:08</p>
    </div>
    <div class="closebuttondiv">
        <form action="" name="deleteReply" method="post">
            <button type="button" class="closebutton" onclick="deleteReplyCheck()">
                <img src="C:\Users\Playdata\Downloads\AlcoholHub-Front_Project-master\AlcoholHub-Front_Project-master\ahub-project\src\assets\free-icon-close-button-61155 (1).png">
            </button>
        </form>
    </div>
    <hr class="replyregistline">
    <div class="registreplywriterdiv">
        <span>안경따거</span>
    </div>
    <div class="registreplydiv">
        <form id="comment" action="" name="registReply" method="post">
            <div class="commentbox">
            <textarea type="text" class="box" id="reply" placeholder="타인의 권리를 침해하거나 명예를 훼손하는 댓글은 운영원칙 및 관련 법률에 의거, 제재를 받을 수 있습니다." required></textarea>
            </div>
            <input type="submit" class="btn" value="등록" onclick="registReplyCheck()">
        </form>
    </div>
    <hr class="replyregistbottomline">
    
</template>

<script setup>

</script>

<style scoped>
    .box {
            width:100%;
            height:100px;
        }
    
    .closebutton{
            border:0px;
            cursor: pointer;
        }

    .btn {
            background-color: #8c52ff;
            color: white;
            padding: 14px 20px;
            margin: 8px 0;
            border: none;
            border-radius: 4px;
            cursor: pointer;
            font-size: 16px;
            font-style: bold;
            float: right;

        }
        .replyline {
            width:95%;
            margin-left: 2%;
            margin-right: 2%;
            height: 2px;
            border: 0;
            background-color: #8c52ff;
        }

        .replyregistline {
            width:95%;
            margin-top: 20%;
            margin-left: 2%;
            margin-right: 2%;
            height: 2px;
            border: 0;
            background-color: #8c52ff;
        }

        .replyregistbottomline {
            width:95%;
            margin-top: 3%;
            margin-left: 2%;
            margin-right: 2%;
            height: 2px;
            border: 0;
            background-color: #8c52ff;
        }

        .replytitlediv {
            margin-top: 10%;
            padding-left: 10px;
            padding-right: 10px;
            margin-left: 2%;
            float: left;
        }

        .replywriterdiv {
            margin-top:2%;
            padding-left: 10px;
            padding-right: 10px;
            margin-left: 2%;
            float: left;
        }

        .replycontentdiv {
            margin-top:2%;
            padding-left: 10px;
            padding-right: 10px;
            margin-left: 2%;
            float: left;
        }

        .closebuttondiv {
            margin-top:2%;
            padding-left: 10px;
            padding-right: 10px;
            margin-right: 5%;
            float: right;
        }
        
        .replydatediv {
            margin-top:2%;
            padding-left: 10px;
            padding-right: 10px;
            margin-left: 22%;
            float: left;
        }

        .registreplywriterdiv{
            margin-top:2%;
            padding-left: 10px;
            padding-right: 10px;
            margin-left: 2%;
            float: left;
        }

        .registreplydiv {
            margin-top: 1%;
            margin-left: 5%;
            float: left;
            width: 75%;
        }

        .replytitle {
            font-size: 20px;
            margin-top: 20px;
        }

        textarea::placeholder {
            font-size:15px;
            padding-left: 1%;
            padding-top: 1%;
        }
</style>