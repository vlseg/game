<template>
    <b-card id="cardfotogr"
            :img-src="require('../img/foto.png')"
            img-alt=""
            img-left class="mb-3"
    >
        <b-card-body title="Svetlakov" id="cardfoto" >
            <b-card-text class="text1">22 May</b-card-text>
            <b-card-text class="text2">
                Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aliquid cumque harum libero molestiae perferendis quam similique. Harum laudantium sunt voluptatem?
            </b-card-text>
        </b-card-body>
    </b-card>
</template>

<script>
    export default {
        name: "CommentFio"
    }
</script>

<style scoped>
    #cardfotogr {
        border-radius: 0;
        border-bottom: 2px solid #302f43;
    }
    .text2 {
        color: #fff;
        font-size: 14px;
    }
    .text1 {
        color: #6b688c;
        font-size: 16px;
        margin-bottom: 13px;
        margin-top: -36px;
        margin-left: 89px;
    }
    #cardfoto img {
        margin-top: 32px;
        margin-right: 20px;
    }
    #cardfoto h4 {
        margin-top: 9px;
    }
    .card-img-left {
        height: 64px;
        margin-right: 23px;
    }
    .card-title {
        color: #9d9acc;
        font-size: 18px;
    }
    .card-body .card-body {
        padding: 0 !important;
    }

</style>