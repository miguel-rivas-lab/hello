<template>
  <main :class="getCity">
    <title>Hello {{ getName }}</title>
    <aside class="texture"></aside>
    <header>
      <h1>Hello<strong>{{ getName }}</strong></h1>
      <img src="./assets/img/cloud.png" class="cloud c01">
      <img src="./assets/img/cloud.png" class="cloud c02">
    </header>
    <section class="letter">
      <div class="container">
        <p>hi!</p>
        <template v-for="(paragraph, index) in letter">
          <p :key="index" v-html="paragraph"/>
        </template>
      </div>
    </section>
    <section class="projects">
      <img src="./assets/img/cloud.png" class="cloud c03">
      <div class="city"/>
    </section>

    <footer>
      <div class="link">
        <a :href="user.website" target="_blank" class="icon website"></a>
        <a :href="user.codepen" target="_blank" class="icon codepen"></a>
        <a :href="user.linkedin" target="_blank" class="icon linkedin"></a>
      </div>
    </footer>
  </main>
</template>

<script lang="ts">
 import Vue from "vue";
 import {letter, user} from "./database";
  const queryString = window.location.search;
  const urlParams = new URLSearchParams(queryString);

  export default Vue.extend({
    data: () => ({
      letter,
      user,
    }),
    computed: {
      getCity(){
        return urlParams.get('city');
      },
      getName(){
        return urlParams.get('name');
      }
    }
  });
</script>