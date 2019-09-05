<template>
    <div class="wrapper">
        <span class="back">
            <i class="fa fa-angle-left left" aria-hidden="true"></i>
            Back
        </span>
        <b-navbar toggleable="lg" type="dark" variant="info" class="cardmenu">
            <b-navbar-nav>

                <b-button size="sm" class="my-2 color" >
                    <i class="fa fa-angle-left left" aria-hidden="true"></i>
                    <span class="spantxt">See Previous</span>
                </b-button>
            </b-navbar-nav>

            <b-navbar-nav class="ml-auto">
                <b-nav-form>
                    <b-button size="sm" class="my-2 color">
                        <span class="spantxtr">See Next</span>
                        <i class="fa fa-angle-right right" aria-hidden="true"></i>
                    </b-button>
                </b-nav-form>

            </b-navbar-nav>
        </b-navbar>

        <b-card
            border-variant="dark"
            tag="article"
            class="mb-2 card"
        >
            <div class="wrapimg">
                <b-card-img
                    :src="require('../img/pagepic.jpg')"
                >
                </b-card-img>
            </div>
            <b-card-body title="The International 2018 Collector’" >
                <b-card-text class="text1">July 24, 2018</b-card-text>
                <b-card-text class="text2">
                    Lorem ipsum dolor sit amet, consectetur adipisicing elit. Accusamus accusantium, autem, cum fugiat harum ipsum modi natus nulla numquam obcaecati omnis optio, porro rerum unde voluptates. A, aut consectetur corporis culpa delectus doloremque earum eos est facilis illum incidunt ipsum labore laboriosam magnam maiores natus, omnis placeat possimus praesentium quam quia quis quo quod rem velit. Atque autem deserunt nemo!
                </b-card-text>
                <b-card-text class="text2">
                    Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aliquid cumque harum libero molestiae perferendis quam similique. Harum laudantium sunt voluptatem?
                </b-card-text>
            </b-card-body>
            <div class="hr"></div>
            <b-card-footer>
                <b-row>
                    <b-col class="laikvis"
                        cols="3"
                        sm="3"
                        md="5"
                        lg="4"
                        xl="6"
                    >
                        <div class="visible" @click="vis"></div>
                        <div class="numlaikclick" @click="vislaik"></div>
                        <b-img id="vispic"
                            :src="require('../img/laiki.jpg')"
                            top=false
                        >
                        </b-img>
                        <p class="laiknum">{{ laikNumValue }}</p>
                        <p class="vislaik">{{ laikVisValue }}</p>
                    </b-col>
                    <b-col class="laikvis"
                        cols="3" offset="5"
                        sm="3" offset-sm="6"
                        md="2" offset-md="4"
                        lg="3" offset-lg="5"
                        xl="3" offset-xl="3"
                    >
                        <div class="odcls" @click="odnoclassniki"></div>
                        <div class="face" @click="facebook"></div>
                        <div class="twitter" @click="twitter"></div>
                        <b-img
                            :src="require('../img/social.jpg')"
                            top=false
                        >
                        </b-img>
                    </b-col>
                </b-row>

            </b-card-footer>
        </b-card>
    </div>
</template>

<script>
    export default {
        name: "LeftPanel",
        data() {
            return {
                laikNumValue: 345,
                laikVisValue: 7.641
            }
        },
        methods: {
            odnoclassniki() {
                window.open("https://ok.ru/", "_blank")
            },
            facebook() {
                window.open("https://www.facebook.com/", "_blank")
            },
            twitter() {
                window.open("https://twitter.com/", "_blank")
            },
            vislaik() {
                this.laikNumValue ++
            },
            vis() {
                this.laikVisValue = +(this.laikVisValue + 0.001).toFixed(3)
            }
        }

    }
</script>

<style scoped>

    .wrapper {
        font-size: 18px;
        width: 100%;
        height: 100%;
        margin-top: 25px;
        text-align: left;
        margin-left: 17px;
    }
    @media only screen and (max-width : 992px) {
        .wrapper {
            margin-left: 0;
        }
    }
    .back {
        margin-bottom: 30px;
    }
    .left {
        color: #9a97c1;
        font-size: 22px;
        margin-right: 10px;
    }
    .right {
        color: #9a97c1;
        font-size: 22px;
        margin-top: 1px;
        margin-left: 10px;
    }
    .cardmenu, .color {
        background: #272637 !important;
        border: none;
        color: #9794c4;
        margin-bottom: 25px;
        border-radius: 15px;
        margin-top: 35px;
        position: relative;
    }
    .card {
        border-radius: 15px;
        background: #242333;
        width: 100%;
    }
    .wrapimg {
        position: relative;
        width: 100%;
        height: 310px;
        overflow: hidden;
        border-radius: 15px;
    }
    .text2 {
        color: #9d9acc;
        font-size: 16px;
    }
    .text1 {
        color: #636182;
        font-size: 16px;
        margin-bottom: 25px;
    }
    .hr {
        position: absolute;
        left: 0;
        height: 2px;
        width: 100%;
        background: #302f43;
        margin-top: 35px;
    }
    .card-body .card-body {
        padding-left: 0 !important;
        padding-bottom: 5px;
    }
    .card-body {
        padding-bottom: 5px;
    }
    .card-footer {
        margin-top: 35px;
        padding-bottom: 0;
        padding-top: 9px;
        padding-left: 0;
    }
    .laiknum {
        position: absolute;
        font-size: 16px;
        top: 24px;
        left: 67px;
    }
    .visnum {
        position: absolute;
        font-size: 16px;
        top: 24px;
        left: 185px;
        color: #9d9acc;
    }
    .laikvis {
        position: relative;
        margin-bottom: 11px;
        padding-top: 14px;
        padding-left: 0;
        display: inline-block;
    }
    .numlaikclick {
        position: absolute;
        top: 22px;
        left: 17px;
        height: 23px;
        width: 24px;
        cursor: pointer;
        background: transparent;
    }
    .visible {
        position: absolute;
        top: 21px;
        left: 122px;
        height: 26px;
        width: 34px;
        cursor: pointer;
        background: transparent;
    }
    .vislaik {
        display: inline-block;
        position: absolute;
        top: 22px;
        left: 169px;
        color: #9d9acc;

    }
    .vispic {
        position: absolute;
        left: 0;
        top: 0;
        padding-top: 18px;
    }
    .spantxt {
        position: absolute;
        top: 5px;
        width: 100px;
    }
    .spantxtr {
        position: absolute;
        right: 15px;
        width: 100px;
        top: 6px;
    }
    .odcls {
        position: absolute;
        background: transparent;
        height: 25px;
        width: 29px;
        left: 7px;
        top: 23px;
        cursor: pointer;
    }
    .face {
        position: absolute;
        background: transparent;
        height: 25px;
        width: 29px;
        left: 52px;
        top: 23px;
        cursor: pointer;
    }
    .twitter {
        position: absolute;
        background: transparent;
        height: 25px;
        width: 29px;
        left: 96px;
        top: 23px;
        cursor: pointer;
    }
</style>