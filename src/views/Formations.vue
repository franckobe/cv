<template>
  <section>
    <h1>
      Formations
    </h1>
    <div>
      <div v-for="formation in formations">
        <h3>{{ formation.title[lang] }} ({{ formation.type[lang] }})</h3>
        <h4>{{ formation.school }}</h4>
        <p>{{ formation.period }}</p>
      </div>
    </div>
  </section>
</template>

<script lang="ts">

export default {
  name: 'Formations',
  props: {
    lang: {
      type: String,
      default: 'fr',
    },
  },
  data() {
    return {
      formations: [
        {
          period: '2017 - 2019',
          school: 'Ynov Aix Campus, Aix-en-Provence',
          type: {
            fr: 'Alternance',
            en: 'Sandwich course',
          },
          title: {
            fr: 'Mastère chef de projet web',
            en: 'Master web project manager',
          },
        },
        {
          period: '2016 - 2017',
          school: 'IUT Aix-Marseille, Aix-en-Provence',
          type: {
            fr: 'Alternance',
            en: 'Sandwich course',
          },
          title: {
            fr: 'Licence professionnelle SIL DA2I',
            en: 'Professional degree SIL DA2I',
          },
        },
        {
          period: '2014 - 2016',
          school: 'Ynov Aix Campus, Aix-en-Provence',
          type: {
            fr: 'Initiale',
            en: 'Initial',
          },
          title: {
            fr: 'BTS Services Informatiques aux Organisations',
            en: 'BTS organizations IT services',
          },
        },
        {
          period: '2012 - 2014',
          school: 'Lycée La Forbine, Marseille',
          type: {
            fr: 'Alternance',
            en: 'Sandwich course',
          },
          title: {
            fr: 'BTS Chimiste',
            en: 'BTS Chemist',
          },
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
  section {
    background-color: transparent;
  }
</style>
