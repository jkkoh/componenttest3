<script>
    export default {
    props: {id:Number,
            title:String, 
            content:String}
}
</script>

<template>
    <div class="blogOuter">
        <p>{{ id }} 번째 포스트</p>
        <h4>제목 : {{ title }}</h4>
        <p>내용 : {{ content }}</p>
    </div>
</template>

<style>
    .blogOuter{
        margin-left: 2vw;
        margin-right: 2vw;
        padding-left: 10px;
        padding-right: 10px;
        padding-bottom: 2px;
        box-sizing: border-box;
        border-top: 1px solid black;
    }
</style>
