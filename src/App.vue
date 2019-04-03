<template>
  <div id="app">
    <header>
      <Navbar :lang="language" @langChanged="changeLang()" />
    </header>
    <main>
      <Presentation class="section" :lang="language" />
      <Experiences class="section" :lang="language" />
      <Competences class="section" :lang="language" />
      <Formations class="section" :lang="language" />
    </main>
  </div>
</template>

<script>
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
        language: 'fr',
      };
    },
    methods: {
      changeLang() {
        this.language = this.language === 'fr' ? 'ang' : 'fr';
      },
    },
  };
</script>

<style lang="scss">
  body {
    margin: 0;
    font-family: Avenir,serif;
    /*
    background: #642B73;
    background: -webkit-linear-gradient(45deg, #642B73, #C6426E);
    background: linear-gradient(45deg, #642B73, #C6426E);
    color: #fff;
    */
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
  }
  section.active {
    opacity: 1;
  }

  a {
    text-decoration: none;
    outline: none;
  }
</style>
