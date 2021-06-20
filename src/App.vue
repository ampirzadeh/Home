<template>
  <div id="app">
      <vs-card v-for="link in links" :key="link.picture" type="5">
    <template #title>
      <h3>{{link.title}}</h3>
    </template>
    <template #img>
      <img :src="link.picture" alt="">
    </template>
    </vs-card>

  </div>
</template>

<script lang="ts">
import Vue from 'vue';

export default Vue.extend({
  name: 'App',
  data() {
    return {
      links: [
        {
          title: 'Whatsapp',
          picture: './whatsapp.jpg'
        },
        {
          title: 'Google',
          picture: './google-1.jpg'
        }
      ]
    }
  }
});
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  padding: 15%;
}
</style>
