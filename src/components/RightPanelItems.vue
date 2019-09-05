<template>
    <div>
        <div class="wrapimg">
            <b-card-img
                :src="require('../img/picleft.jpg')"
                style="border-radius: 15px"
            >
            </b-card-img>
        </div>
        <b-card
            tag="article"
            class="mb-2 card"
        >
            <b-card-body title="Welcome to Nethernite" >
                <b-card-text>
                    Some quick example text to build on the card title and make up the bulk of the card's content.
                </b-card-text>
            </b-card-body>
        </b-card>
    </div>
</template>

<script>
    export default {
        name: "RightPanelItems"
    }
</script>

<style scoped>
    .wrapimg {
        position: relative;
        width: 100%;
        height: 150px;
        overflow: hidden;
        margin-top: 34px;
    }
    .card {
        background: #242333;
        width: 100%;
        border-radius: 0 0 15px 15px;
    }
    p {
        color: #9d9acc;
        font-size: 14px;
    }
    h4 {
        font-size: 18px;
        margin-bottom: 5px;
    }
    .card-body .card-body {
        padding: 0 0 0 0;
    }

</style>