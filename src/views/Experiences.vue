<template>
  <section>
    <h1>
      Expériences
    </h1>
    <div>
      <div v-for="experience in experiences">
        <h3>{{ experience.title[lang] }}</h3>
        <div>
          <p>{{ experience.period[lang] }}</p>
          <p>{{ experience.type[lang] }}</p>
          <p>{{ experience.company }}</p>
        </div>
        <ul>
          <li v-for="mission in experience.missions">
            {{ mission[lang] }}
          </li>
        </ul>
      </div>
    </div>
  </section>
</template>

<script lang="ts">

export default {
  name: 'Experiences',
  props: {
    lang: {
      type: String,
      default: 'fr',
    },
  },
  data() {
    return {
      experiences: [
        {
          period: {
            fr: 'septembre 2016 - septembre 2019 (3 ans)',
            ang: 'september 2016 - september 2019 (3 years)',
          },
          company: 'Préparatoire Delpech Marseille, Marseille',
          type: {
            fr: 'Contrat de professionnalisation',
            ang: 'Professionalisation contract',
          },
          title: {
            fr: 'Développeur Fullstack',
            ang: 'Fullstack Developer',
          },
          missions: [
            {
              fr: 'Développement d\'un intranet et d’un site internet avec espace client',
              ang: 'Development of an intranet and a website with customer area',
            },
            {
              fr: 'Développement d\'applications natives Android et IOS',
              ang: 'Development of Android and iOS native applications',
            },
            {
              fr: 'Développement d\'outils web pour statistiques et historique',
              ang: 'Development of web tools for statistics and history',
            },
          ],
        },
        {
          period: {
            fr: 'janvier 2016 - février 2016 (2 mois)',
            ang: 'january 2016 - february 2016 (2 months)',
          },
          company: 'Silae, Luynes',
          type: {
            fr: 'Stage',
            ang: 'Internship',
          },
          title: {
            fr: 'Développeur web',
            ang: 'Web Developer',
          },
          missions: [
            {
              fr: 'Participation à la refonte du site de présentation de Silaexpert : ' +
                      'création d\'un template et de modules Joomla',
              ang: 'Redesign of Silaexpert\'s website : creation of template and mofules for Joomla',
            },
          ],
        },
        {
          period: {
            fr: 'juin 2015 - juillet 2015 (2 mois)',
            ang: 'jun 2015 - july 2015 (2 months)',
          },
          company: 'Communauté d\'Agglomération du Pays de Martigues, Martigues',
          type: {
            fr: 'Stage',
            ang: 'Internship',
          },
          title: {
            fr: 'Développeur',
            ang: 'Developer',
          },
          missions: [
            {
              fr: 'Développement d\'une application WinDev et d\'une page web pour partage de fichiers',
              ang: 'Development of a Windev application with a web module for file sharing',
            },
            {
              fr: 'Mise à jour du mode de connexion de deux sites Web (PDO)',
              ang: 'Rewrite the connection mode of two websites to PDO',
            },
          ],
        },
        {
          period: {
            fr: 'juin 2015 - juillet 2015 (2 mois)',
            ang: 'jun 2015 - july 2015 (2 months)',
          },
          company: 'SGS Oil Gas & Chemicals, Martigues',
          type: {
            fr: 'Contrat de professionnalisation',
            ang: 'Professionalisation contract',
          },
          title: {
            fr: 'Opérateur chimiste',
            ang: 'Chemist operator',
          },
          missions: [
            {
              fr: 'Échantillonnage et jaugeage dans l’industrie pétrolière, les navires et les stations-services',
              ang: 'Sampling and gauging in petroleum industry, ships and service stations',
            },
            {
              fr: 'Contact et prises de rendez-vous téléphoniques avec la clientèle',
              ang: 'Contact and appointments with customers',
            },
          ],
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
