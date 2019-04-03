<template>
  <section>
    <h1>
      Franck Garros
    </h1>
    <p>
      Actuellement en Mastère 2 Chef de projet web, et en alternance au Préparatoire Delpech Marseille,
      je termine mon contrat en septembre 2019. Date à partir de laquelle je serai disponible pour un nouveau poste !
    </p>
    <p>
      Durant mes 3 ans au sein de cette entreprise, j'ai pu réaliser un intranet, un site internet avec espace client,
      une application native Android et iOS, ainsi que de multiple outils web.
    </p>
  </section>
</template>

<script>
export default {
  name: 'Presentation',
  props: {
    lang: {
      type: String,
      default: 'fr',
    },
  },
};
</script>

<style lang="scss" scoped>
  p {
    text-align: center;
  }
</style>
