<template>
  <v-app>
    <div id="app">
      <video-bg :sources="['./static/video/stairsvideo.mp4']" img="./assets/logo.png">
        <div id="toolbar-image">
          <v-toolbar class="transparent elevation-0" light>
            <v-toolbar-title class="hidden-sm-and-down">Toolbar</v-toolbar-title>
            <v-spacer></v-spacer>
            <v-toolbar-items>
              <v-toolbar-item v-for="item in items" :key="item">
                {{ item.title }}
              </v-toolbar-item>
            </v-toolbar-items>
          </v-toolbar>
          <stairs-tab class="centered"></stairs-tab>

        </div>
      </video-bg>
    </div>
  </v-app>
</template>

<script>
  import VideoBg from 'vue-videobg'
  import StairsTab from './components/StairsTab.vue'
  export default {
    name: 'app',
    components: {VideoBg, StairsTab},
    data () {
      return {
        items: [
          {title: 'About'},
          {title: 'My Score'},
          {title: 'High Scores'}
        ]
      }
    }
  }
</script>

<style>
  #toolbar-image {
    background: url('http://ww.powerpointhintergrund.com/uploads/2017/05/simple-backgrounds-wallpaper-2560x1440--47279-31.jpeg');
  }

  .centered {
    position: fixed; /* or absolute */
    top: 50%;
    left: 50%;
    transform: translateX(-50%) translateY(-50%);
    width: 512px;
  }

</style>
