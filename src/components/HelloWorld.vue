<template>
  <v-container>
    <v-row class="text-center">
      <v-col cols="12">
        <v-img :src="logo" class="my-3" contain height="200" />
      </v-col>

      <v-col class="mb-4">
        <h1 class="display-2 font-weight-bold mb-3">
          Tauri + Vite + Vue3 + Vuetify3 + TypeScript
        </h1>

        <h4>Video Player Testing</h4>

        <p class="subheading font-weight-regular">
          For display video streaming
        </p>
      </v-col>
    </v-row>
    <v-row class="text-center">
      <video width="480" height="360" controls>
        <source src="http://172.16.1.93/mjpg/1/video.mjpg" type="video/mjpg" />
        Your browser does not support the video tag.
      </video>
    </v-row>
  </v-container>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import { VideoJsPlayer } from 'video.js';
import { VideoPlayer } from '@videojs-player/vue';
import 'video.js/dist/video-js.css';

// Logo
import logo from '../assets/logo.svg';

export default defineComponent({
  name: 'HelloWorld',
  components: {
    VideoPlayer,
  },
  data() {
    return {
      logo,
    };
  },
});
</script>
