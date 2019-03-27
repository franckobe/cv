<template>
  <div id="app">
    <header>
      <Navbar />
    </header>
    <main id="fullpage">
      <Presentation data-anchor="presentation" class="section" />
      <Experiences data-anchor="experiences" class="section" />
      <Competences data-anchor="competences" class="section" />
      <Formations data-anchor="formations" class="section" />
    </main>
  </div>
</template>

<script lang="ts">
  import Presentation from '@/views/Presentation.vue';
  import Navbar from '@/components/Navbar.vue';
  import Experiences from '@/views/Experiences.vue';
  import Competences from '@/views/Competences.vue';
  import Formations from '@/views/Formations.vue';

  export default {
    components: {
      Navbar,
      Presentation,
      Experiences,
      Competences,
      Formations,
    },
    data() {
      return {

      };
    },
  };
</script>

<style lang="scss">
  body {
    margin: 0;
    font-family: Avenir,serif;
    background: #642B73;  /* fallback for old browsers */
    background: -webkit-linear-gradient(45deg, #642B73, #C6426E);  /* Chrome 10-25, Safari 5.1-6 */
    background: linear-gradient(45deg, #642B73, #C6426E); /* W3C, IE 10+/ Edge, Firefox 16+, Chrome 26+, Opera 12+, Safari 7+ */
  }
  * {
    position: relative;
    box-sizing: border-box;
  }
  #app {
    display: flex;
  }
  header {
    width: 300px;
    height: 100vh;
    position: sticky;
    top: 0;
  }
  main {
    flex-grow: 1;
    min-height: 100vh;
    max-width: calc(100% - 300px) !important;
  }

  section {
    // height: 100vh;
    // overflow-y: auto;
    padding: 40px;
    opacity: 0;
  }
  section.active {
    opacity: 1;
  }

  a {
    text-decoration: none;
    outline: none;
  }
</style>
