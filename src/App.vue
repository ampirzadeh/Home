<template>
  <div id="app">
    <vs-row class="container">
      <vs-col v-for="link in links" :key="link.picture" xs="12" sm="5" lg="3" style="margin: 50px auto auto 10px">
        <a :href="link.link">
          <vs-card type="2">
            <template #text>
              <h3 v-text="link.title" />
            </template>
            <template #img>
              <img :src="link.picture" :alt="link.title" />
            </template>
          </vs-card>
        </a>
      </vs-col>
    </vs-row>
  </div>
</template>

<script lang="ts">
import Vue from "vue";

export default Vue.extend({
  name: "App",
  data() {
    return {
      links: [
        {
          title: "Whatsapp",
          link: "https://web.whatsapp.com/",
          picture: "images/whatsapp.jpg",
        },
        {
          title: "Google",
          link: "https://google.com",
          picture: "images/google-1.jpg",
        },
        {
          title: "Google",
          link: "https://google.com",
          picture: "images/google-2.jpg",
        },
        {
          title: "Twitter",
          link: "https://twitter.com",
          picture: "images/twitter.jpg",
        },
      ],
    };
  },
});
</script>

<style>
html,
body {
  height: 100%;
  width: 100%;
}
html,
body,
#app {
  overflow: hidden;
  margin: 0px;
  padding: 0px;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  background-image: linear-gradient(to bottom right, #2c3e50, #04090e);
  color: #2c3e50;
  padding: 8%;
  height: 100%;
}
</style>
