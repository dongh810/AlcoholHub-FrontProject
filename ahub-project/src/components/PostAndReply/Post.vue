<template>
    <div class="wrapper">
        <section>
            <h1 class="boardname">후기 게시판</h1>
            <hr class="boardtitleLine">
        </section>
        <div class="boardtitlediv">
            <h2 class="boardtitle"> 간으로 써내려간 지난날의 1-10만원 와인</h2>
        </div>
        <div class="writerdiv">
            <h3 class="writer"></h3>
        </div>
        <div class="datediv">
            <h3 class="date">2024.03.16 9:31:01</h3>
        </div>
        <hr class="titleLine">
        <div class="maincontent">
            <p>
                오늘은 그냥 짧디짧은 제 구력에 한번씩 스파크를 튀긴 와인들을 한번 써볼려 합니다. 
                지극히 사심이 가득히 담긴 글이라 지나가셔도 됩니다. 
                <br><br>
                이 글은 제 개인이 글이라 항상 공지에 있는 추천 와인들처럼, 구하기 쉽거나 인지도 있는
                친구들은 별로 안나오고, 심지어 안팔려서 국내에서 더이상 수입이 멈춘 안타까운 녀석들도 있으니
                <br><br>
                혹여나 글을 읽고 찾으려 해도 생각보다 주변에 안나올수 있는점 양해를^~^
            </p>
        </div>

        <Reply/>
    </div>
</template>

<script setup>
    import Reply from './Reply.vue';
    import axios from "axios";

    import {ref} from "vue";

    const post = ref(null);

    const fetchPost = async () => {
        try {
            const response = await axios.get('http://localhost:8081/post');
            if (response.data && Array.isArray(response.data) && response.data.length > 0) {
                console.log(post.value = response.data[0]);
                
            } else {
                console.error('게시글 데이터가 비어있습니다.');
            }
        } catch (error) {
            console.error('데이터 로드 중 오류 발생:', error);
        }
    };

    


    

    
</script>

<style scoped>
    

        .boardtitleLine {
            width:100%;
            height: 3px;
            border: 0;
            background-color: #8c52ff;
        }

        .titleLine {
            width:95%;
            margin-left: 2%;
            margin-right: 2%;
            height: 2px;
            border: 0;
            background-color: grey;
        }

        .wrapper {
            height: auto;
            min-height: 100%;
            width: 68%;
            margin-top: 50px;
            padding-bottom: 100px;
            margin-left: 16%;
            margin-right: 16%;
        }

        .boardname {
            font-size: 32px;
        }

        .boardtitle {
            font-size: 20px;
            margin-top: 20px;
        }

        .writer {
            font-size: 16px;
            margin-top: 25px;
        }

        .date {
            font-size: 16px;
            margin-top: 25px;
        }

        .boardtitlediv {
            padding-left: 10px;
            padding-right: 10px;
            margin-left: 2%;
            float: left;
        }

        .writerdiv {
            margin-left: 43%;
            float:left;
        }

        .datediv {
            padding-right: 10px;
            margin-right: 2%;
            float:right;
        }

        

        .maincontent {
            max-width: 80%;
            margin-left: 10%;
            margin-right: 10%;
            margin-top: 3%;
        }

        
</style>