<template>
  <div id="app">

    <b-container>
      <b-row>
        <b-col class="d-flex justify-content-center"
          cols="1"
          sm="1"
          md="1"
          lg="6"
          xl="6" offset-xl="1"
        >
          <MainMenu />
        </b-col>
        <b-col class="d-flex justify-content-center"
          cols="7" offset="3"
          sm="3" offset-sm="7"
          md="3" offset-md="8"
          lg="3" offset-lg="3"
          xl="3" offset-xl="2"
        >
          <Profil />
        </b-col>
      </b-row>

      <b-row style="background:transparent !important; max-height: 100%">
        <b-col md="7">
          <LeftPanel />
        </b-col>
        <b-col md="5">
          <RightPanel />
        </b-col>
      </b-row>

      <b-row style="background:transparent !important; max-height: 100%">
        <b-col xl="7" order-xl="1">
          <BottomPanel />
        </b-col>
      </b-row>

    </b-container>
  </div>
</template>

<script>
import MainMenu from './components/MainMenu.vue'
import Profil from './components/Profil.vue'
import LeftPanel from './components/LeftPanel.vue'
import RightPanel from './components/RightPanel.vue'
import BottomPanel from './components/BottomPanel.vue'

export default {
  name: 'app',
  components: {
    MainMenu,
    Profil,
    LeftPanel,
    RightPanel,
    BottomPanel
  }
}
</script>

<style>
  #app {
    font-family: 'Geomantist', sans-serif;
    font-size: 14px;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #fff;
    background: #282828;
    height: 100vh;
  }
  .container {
    background: #323145 url('./img/img_bgс.jpg') no-repeat;
    max-width: 1366px !important;
    min-width: 400px;
    margin: 0 auto !important;
  }
  @font-face {
      font-family: 'Geomantist';
      src: url('../fonts/Geomanist-Book.otf');
  }
  #app .row {
    background-color: #252434 !important;
    max-height: 73px;
  }
  @media only screen and (max-width : 992px) {
    #app .row {
      max-height: none;
    }
  }
</style>
