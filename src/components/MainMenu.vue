<template>
    <div style="width: 100%;" >
        <b-navbar toggleable="lg" type="dark" variant="dark" class="burg">

                <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

                <b-collapse id="nav-collapse" is-nav >
                    <b-navbar-nav left>
                        <b-nav-item href="#">Home</b-nav-item>
                        <b-nav-item href="#">Marketplace</b-nav-item>
                        <b-nav-item href="#">Booster Packs</b-nav-item>
                    </b-navbar-nav>
                    <div class="buttplay">
                        <div class="circle"></div>
                        <b-button size="sm" class="my-2 my-sm-0 " type="submit">Play</b-button>
                    </div>
                    <div style="height: 60px"></div>
                </b-collapse>
            </b-navbar>
    </div>
</template>

<script>
    export default {
        name: "MainMenu",
    }
</script>

<style scoped>
    .navbar-dark .navbar-nav .nav-link{
        color: #ffffff !important;
        height: 63px;
        width: 104px;
        padding-top: 15px;
    }
    .burg {
        margin-top: 6px;
    }
    .buttplay {
        position: relative;
        margin-top: -52px;
    }
    .navbar-dark .navbar-toggler {
        margin-bottom: 16px;
        border-color: #252434;
    }
    .navbar-nav a:nth-child(1):hover {
        border-bottom: 2px solid;
        border-image: linear-gradient(to right, #b44c9c, #c9725d ) 100% 0;
    }
    .navbar-nav a:nth-child(2):hover {
        border-bottom: 2px solid;
        border-image: linear-gradient(to right, #b44c9c, #c9725d ) 100% 0;
    }
    .navbar-nav a:nth-child(3):hover {
        border-bottom: 2px solid;
        border-image: linear-gradient(to right, #b44c9c, #c9725d ) 100% 0;
    }
    .navbar-nav li:nth-child(2) {
        padding-left: 21px;
    }
    .navbar-nav li:nth-child(3) {
        padding-left: 53px;
        width: 200px;
    }
    .bg-dark {
        background: transparent !important;
        margin-left: 107px;
        padding-bottom: 0;
        padding-top: 2px;
    }
    .btn {
        width: 103px;
        height: 41px;
        left: 0;
        top: 0;
        border-radius: 50px;
        padding-left: 0;
        padding-top: 0;
        background-color: #252434;
        position:absolute;
        z-index:2;
    }
    .circle {
        border-radius: 50px;
        background-image: linear-gradient(to right, #6f6d99 0%, #9c99cb 100%);
        width: 107px;
        height:43px;
        top: -1px;
        left: -2px;
        position:absolute;
        z-index:1;
    }
    @media only screen and (max-width : 992px) {
        .burg {
            margin-top: 13px;
            margin-left: 0;
        }
        .buttplay {
            position: relative;
            margin-top: 7px;
        }
        .navbar-nav li:nth-child(1) {
            text-align: left;
            padding-left: 14px;
            height: 40px;
        }
        .navbar-nav li:nth-child(1) a {
            padding-top: 8px !important;
        }
        .navbar-nav li:nth-child(1) :hover {
            color: #000000 !important;
            border-bottom: none;
        }
        .navbar-nav li:nth-child(1):hover {
            background: white;
        }
        .navbar-nav li:nth-child(2) {
            text-align: left;
            padding-left: 14px;
            height: 40px;
        }
        .navbar-nav li:nth-child(2) a {
            padding-top: 8px !important;
        }
        .navbar-nav li:nth-child(2) :hover {
            color: #000000 !important;
            border-bottom: none;
        }
        .navbar-nav li:nth-child(2):hover {
            background: white;
        }
        .navbar-nav li:nth-child(3) {
            text-align: left;
            padding-left: 14px;
            height: 40px;
        }
        .navbar-nav li:nth-child(3) a {
            padding-top: 8px !important;
        }
        .navbar-nav li:nth-child(3) :hover {
            color: #000000 !important;
            border-bottom: none;
        }
        .navbar-nav li:nth-child(3):hover {
            background: white;
        }
        .navbar-nav li:nth-child(3) {
            text-align: left;
            padding-left: 14px;
            margin-bottom: 13px;
            height: 40px;
        }
        .nav-item li:hover {
            background: #fff;
            color: black !important;
            border-bottom: none;
        }
    }
    @media only screen and (max-width : 575px) {
        .btn {
            top: -8px;
        }
    }

</style>