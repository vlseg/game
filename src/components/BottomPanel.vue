<template>
    <div class="wrapper">
        <b-card
            border-variant="dark"
            tag="article"
            class="mb-2 card"
        >
            <b-card-body >
                <b-row>
                    <b-col class="comment">
                        <div class="numcomclick" @click="viscom"></div>
                        <b-img
                            :src="require('../img/comment.jpg')"
                            top=false
                        >
                        </b-img>
                        <p class="numcom">{{ valuecom }}</p>
                    </b-col>
                    <b-col>
                        <b-navbar type="dark" variant="dark"  class="nav justify-content-end">
                            <b-navbar-nav>
                                <b-nav-item href="#">Popular</b-nav-item>
                                <b-nav-item href="#" style="width: 38px"></b-nav-item>
                                <b-nav-item href="#">Recent</b-nav-item>
                            </b-navbar-nav>
                        </b-navbar>
                    </b-col>
                </b-row>
                <div class="hr"></div>

                <b-input-group class="mt-3 typecom">
                    <b-form-input id="input-default" placeholder="Type comment here.."></b-form-input>
                    <b-input-group-append>
                        <b-button id="btnn"></b-button>
                    </b-input-group-append>
                </b-input-group>
                <CommentFio />
                <CommentFio />
            </b-card-body>
        </b-card>
    </div>
</template>

<script>
    import CommentFio from './CommentFio.vue'

    export default {
        name: "BottomPanel",
        data() {
            return {
                valuecom: 48
            }
        },
        methods: {
            viscom() {
                this.valuecom ++
            }
        },
        components: {
            CommentFio
        }
    }
</script>

<style scoped>

    .wrapper {
        font-size: 18px;
        width: 100%;
        height: 100%;
        margin-top: 12px;
        text-align: left;
        margin-left: 17px;
    }
    @media only screen and (max-width : 992px) {
        .wrapper {
            margin-left: 0;
        }
    }
    .card {
        border-radius: 15px;
        background: #242333;
        width: 100%;
        padding-bottom: 30px;
    }
    .hr {
        position: absolute;
        left: 0;
        height: 2px;
        width: 100%;
        background: #302f43;
        margin-top: -10px;
        z-index: 1;
    }
    .comment {
        position: relative;
        padding-left: 4px;
    }
    .numcom {
        position: absolute;
        left: 172px;
        top: 8px;
    }
    .numcomclick {
        position: absolute;
        top: 11px;
        left: 27px;
        height: 22px;
        width: 134px;
        cursor: pointer;
        background: transparent;
    }
    .card-body .card-body {
        padding: 0 !important;
    }
    .bg-dark {
        margin-top: -17px;
        background: #252434 !important;
    }
    li {
        padding-bottom: 17px;
        margin-top: 9px;
        font-family: "MyriadProRegular";
        font-size: 18px;
    }
    li:nth-child(1):hover {
        border-bottom: 2px solid;
        border-image: linear-gradient(to right, #b44c9c, #c9725d ) 100% 0;
        z-index: 2;
    }
    li:nth-child(3):hover {
        border-bottom: 2px solid;
        border-image: linear-gradient(to right, #b44c9c, #c9725d ) 100% 0;
        z-index: 2;
    }
    @font-face {
        font-family: "MyriadProRegular";
        src: url("../../fonts/MyriadProRegular.otf");
        font-style: normal;
    }
    .nav-link {
        color: #9d9acc !important;
    }
    .nav-link:hover {
        color: white !important;
    }
    #input-default {
        height: 60px;
        background: #2a293b !important;
        border: none;
    }
    #btnn {
        background-image: url('../img/strleft.jpg');
        background-repeat: no-repeat;
        background-position: center;
        background-color: #2a293b !important;
        border: none;
    }
    .typecom {
        margin-bottom: 34px;
    }
    .input-group-append {
        padding-right: 30px;
        padding-left: 6px;
        background: #2a293b;
    }

</style>