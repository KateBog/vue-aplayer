<template>
  <div id="app">
    <div class="container">
      <h1 align="center">SocialTech</h1>
      <h3>Simple audio player</h3>
      <aplayer
          :is-loaded="isLoaded"
          theme="#35495e"
          :music="{ src }"
          @load="load"
      />
      http://0.0.0.0:3000/aplayer/secretbase.mp3
      <!--<h3>Featured</h3>-->
      <!--<aplayer-->
      <!--autoplay-->
      <!--theme="pic"-->
      <!--shuffle-->
      <!--repeat="list"-->
      <!--show-lrc-->
      <!--:muted.sync="muted"-->
      <!--:volume.sync="volume"-->
      <!--:music='list3[0]'-->
      <!--:list='list3'-->
      <!--/>-->
      <!--<h3>Mini mode / Float mode (try dragging it around)</h3>-->
      <!--<aplayer-->
      <!--mini-->
      <!--float-->
      <!--:music="{-->
      <!--title: 'トリカゴ',-->
      <!--artist: 'XX:me',-->
      <!--src: 'http://0.0.0.0:3000/aplayer/darling.mp3',-->
      <!--}"-->
      <!--/>-->
    </div>
  </div>
</template>
<script>
  import Aplayer from '../vue-aplayer.vue'

  export default {
    name: 'App',
    components: {
      Aplayer,
    },
    methods: {
      load (a, b) {
        // alert('fire')

        this.src = [{
          src: 'http://0.0.0.0:3000/aplayer/secretbase.mp3',
          type: 'audio/mp3',
        }]
        this.isLoaded = true
      },
    },
    data () {
      return {
        version: VERSION,
        volume: 1,
        muted: false,
        music3: null,
        src: null,
        isLoaded: false,
        list3: [
          {
            title: 'sfsdfs',
            artist: 'asdfasfd',
            src: 'http://0.0.0.0:3000/aplayer/yourname.mp3',
            pic: 'http://0.0.0.0:3000/aplayer/yourname.jpg',
            lrc: 'http://0.0.0.0:3000/aplayer/yourname.lrc',
          },
          {
            title: 'asdfasfasdfas.m3u8',
            artist: 'Goose house',
            src: 'http://0.0.0.0:3000/aplayer/hls/hikarunara.m3u8',
            pic: 'http://0.0.0.0:3000/aplayer/hikarunara.jpg',
            lrc: 'http://0.0.0.0:3000/aplayer/hikarunara.lrc',
          },
          {
            title: 'asdfasfgfdg',
            artist: 'asdfasdfas',
            src: 'http://0.0.0.0:3000/aplayer/snowmoonflowers.mp3',
            pic: 'http://0.0.0.0:3000/aplayer/snowmoonflowers.jpg',
            lrc: 'http://0.0.0.0:3000/aplayer/snowmoonflowers.lrc',
          },
          {
            title: 'asdfasdfas!',
            artist: 'asdfasf',
            src: 'http://0.0.0.0:3000/aplayer/yuruyuri.mp3',
            pic: 'http://0.0.0.0:3000/aplayer/yuruyuri.jpg',
            lrc: 'http://0.0.0.0:3000/aplayer/yuruyuri.lrc',
          },
        ],
      }
    },
  }
</script>
<style>
  html, body {
    width: 100%;
    height: 100%;
    margin: 0;
    padding: 0;
    overflow: hidden;
  }

  body {
    font-family: Source Sans Pro, 'PingFang SC', 'Helvetica Neue', Helvetica, Arial, sans-serif;
    background: linear-gradient(135deg, rgb(65, 184, 131), rgb(74, 156, 238));
    color: #fff;
    overflow-y: auto;
  }

  #app {
    text-align: center;
  }

  .container {
    max-width: 32rem;
    margin-left: auto;
    margin-right: auto;
    margin-bottom: 50px;
    padding: 0 15px;
  }

  h1 {
    font-size: 48px;
    margin: 30px 0 10px;
  }

  h3 {
    font-size: 24px;
  }

  input {
    background-color: transparent;
    outline: none;
    border: none;
    color: inherit;
    font-size: inherit;
    text-align: center;
    border-bottom: 1px solid rgba(255, 255, 255, .5);
  }

  a {
    color: #35495e;
    text-decoration: none;
  }

  p {
    font-size: 18px;
  }
</style>