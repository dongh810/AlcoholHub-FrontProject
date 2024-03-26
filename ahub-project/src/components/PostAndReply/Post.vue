<template>
    <div class="wrapper">
        <section>
            <h1 class="boardname">후기 게시판</h1>
            <hr class="boardtitleLine">
        </section>
        <div class="boardtitlediv">
            <h2 class="boardtitle"> {{posts.postTitle}}</h2>
        </div>
        <div class="writerdiv">
            <h3 class="writer"></h3>
        </div>
        <div class="datediv">
            <h3 class="date">{{posts.postDate}}</h3>
        </div>
        <hr class="titleLine">
        <div class="maincontent">
            <p>
                {{ posts.postContent }}
            </p>
        </div>

        <Reply/>
    </div>
</template>

<script setup>
    import Reply from './Reply.vue';
    import axios from "axios";
    import { ref } from "vue";

    const posts = ref([]);

    const fetchPosts = (postId) => {
        axios.get("http://localhost:8080/post?${postId}")
        .then(response => {
            posts.value = response.data[0];
            console.log(posts.value);
            console.log(posts.value.title);
        })
    }

    fetchPosts(2);

    


    

    
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