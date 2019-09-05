<template>
    <div class="profil">
        <div class="visible" @click="vis"></div>
        <div class="numkrclick" @click="viskr"></div>
        <b-img style="margin-top: 6px;"
           :src="require('../img/profil.jpg')" alt="Profil">
        </b-img>
        <b-img class="znak1" v-if="vis1"
           :src="require('../img/znak1.png')" alt="">
        </b-img>
        <b-img class="znak2" v-if="vis2"
           :src="require('../img/znak2.png')" alt="">
        </b-img>
        <p class="numkr">{{ valuekr }}</p>
    </div>
</template>

<script>
    export default {
        name: "Profil",
        data() {
            return {
                vis1: true,
                vis2: true,
                valuekr: 142
            }
        },
        methods: {
            vis() {
                this.vis1 = !this.vis1;
                this.vis2 = !this.vis2;
            },
            viskr() {
                this.valuekr ++
            }
        }
    }
</script>

<style scoped>
    .profil {
        position: relative;
    }
    .znak1 {
        position: absolute;
        left: 29px;
        top: 19px;
    }
    .znak2 {
        position: absolute;
        left: 88px;
        top: 19px;
    }
    .numkr {
        position: absolute;
        font-size: 14px;
        top: 25px;
        left: 168px;
    }
    .numkrclick {
        position: absolute;
        top: 26px;
        left: 137px;
        height: 20px;
        width: 21px;
        cursor: pointer;
        background: transparent;
    }
    .visible {
        position: absolute;
        top: 10px;
        left: 227px;
        height: 50px;
        width: 50px;
        cursor: pointer;
        background: transparent;
    }
    @media (min-width: 1024px) and (max-width: 1234px) {
        .profil {
            margin-right: 46px;
        }
    }
    @media (min-width: 576px) and (max-width: 1024px) {
        .profil {
            margin-right: 100px;
        }
    }

</style>