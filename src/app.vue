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
        <p>I am <em>Miguel Rivas</em> a Frontend Developer who lives in Santo Domingo and I'm looking forward to join your team. I've been working for a while developing websites for top brands as Cerveza Presidente.</p>
        <p>It has been a really good journey but right now i'll like to expand my knowledge and explore the best practices around the world.</p>
        <p>I've been working with tools like Github, Jade/Haml, Sass/Less And PHP/Ruby. I hope my portfolio can get your attention, since i'm really interested in learning more of FromAtoB.</p>
        <p>In the bottom i attached my portfolio, codepend account, linkedin profile and e-mail.</p>
        <p>I'm really looking forward to hear from you. <em>:)</em></p>
      </div>
    </section>
    <section class="projects">
      <h2>Some<strong>Projects</strong></h2>
      <a>
        <img src="./assets/img/dr-logic.jpg">
      </a>
      <a>
        <img src="./assets/img/evolution.jpg">
      </a>
      <a>
        <img src="./assets/img/presidente.jpg">
      </a>
      <a>
        <img src="./assets/img/screen.jpg">
      </a>
      <a>
        <img src="./assets/img/gear.jpg">
      </a>
      <a>
        <img src="./assets/img/css.jpg">
      </a>
      <a>
        <img src="./assets/img/windows.jpg">
      </a>
      <img src="./assets/img/cloud.png" class="cloud c03">
      <div class="city"/>
    </section>

    <footer>
      <h2>Contact Me</h2>
      <div class="link">
        <a href="https://miguel-rivas.github.io/" target="_blank" class="icon website"></a>
        <a href="http://codepen.io/planet-wurlex/" target="_blank" class="icon codepen"></a>
        <a href="https://www.linkedin.com/in/jesus-rivas-b43936184/" target="_blank" class="icon linkedin"></a>
      </div>
    </footer>
  </main>
</template>

<script lang="ts">
 import Vue from "vue";
  const queryString = window.location.search;
  const urlParams = new URLSearchParams(queryString);

  export default Vue.extend({
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