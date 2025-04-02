<template>
    <div
        class="v-page-index"
    >
      <AppHeader/>


      <AppSection
              title="Voyage Exploratoire"
              subtitle="À la découverte de nouvelles façons de faire des lieux à impact social"
              svg_path="shapes/section_A.mp4"
              uniq_id="section_00"
              :is_open="true"
      >
        <p>Ce voyage au départ de Genève, prend la forme d’un voyage immersif à travers la francophonie pour découvrir les espaces communs qui soutiennent le changement de dynamique sociale de notre société.</p>
        <p>Et pour ambition, pour son retour en terres genevoises, de donner l’impulsion afin de créer et réinventer des lieux ayant un impact social et culturel nouveau grâce aux apprentissages acquis durant l’exploration.</p>
        <p>Le voyage est construit avec comme base les besoins, les questionnements et les connaissances des participant·es.</p>
      </AppSection>

      <AppSection
              title="En bref"
              svg_path="shapes/section_B.mp4"
              uniq_id="section_01"
      >
        <p>En 2024, ce sont plus de 35 acteur·ices pluridisciplinaires genevois, tel·les que des travailleur·ses sociaux, des architectes, des urbanistes, des acteur·rices institutionnels, représentants de fondations privées, ainsi que des personnes en charge de gérer des lieux à finalité sociale qui embarquent pour le 1er voyage exploratoire.</p>
        <p>Ce voyage au départ de Genève, prend la forme d’un voyage immersif à travers la francophonie pour découvrir les espaces communs qui soutiennent le changement de dynamique sociale de notre société.</p>
        <p>Et pour ambition, pour son retour en terres genevoises, de donner l’impulsion afin de créer et réinventer des lieux ayant un impact social et culturel nouveau grâce aux apprentissages acquis durant l’exploration.  Le voyage est construit avec comme base les besoins, les questionnements et les connaissances des participant·es.</p>
        <p>Concrètement, chaque inscription donne lieu à un entretien avec un des membres de l’équipe. La synthèse de ces besoins est partagée dans un temps collectif en amont du voyage. Sur 3 jours, les 35 participant·es partent dans 3 villes différentes (Paris, Bruxelles, Marseille) pour rencontrer des porteurs de projets inspirants et analyser les dynamiques locales. Il repose sur des principes fondamentaux tels que l’immersion, la transmission des savoirs, la co-construction et l’expérimentation.</p>
        <p>Pour s’assurer d’un voyage répondant aux enjeux des acteur·rices du territoire, il est important de le construire avec des acteur·rices déjà au contact des réflexions et expérimentations autour de ces lieux.</p>

        <p>Objectifs</p>
        <ul>
          <li>Découvrir des espaces novateurs et apprendre de leurs pratiques</li>
          <li>Acquérir des outils et méthodologies pour concevoir et animer des lieux</li>
          <li>Documenter et partager les apprentissages pour enrichir les pratiques à Genève</li>
        </ul>
      </AppSection>


      <AppSection
              title="Un dispositif en﻿ plusieurs phases"
              svg_path="shapes/section_C.mp4"
              uniq_id="section_02"
      >
        <app-timeline
                :items="timelineContent"
        />

        <h4>Des entretiens individuels et une rencontre préliminaire</h4>
        <h4>1. Préparation (Genève)</h4>

        <p>Avant le départ, les participants se retrouvent pour :</p>

        <ul>
          <li>Se familiariser avec les concepts et outils d’analyse</li>
          <li>Définir les axes de documentation</li>
          <li>Préparer leur parcours</li>
        </ul>

        <h4>2. Exploration (Paris, Bruxelles, Marseille)</h4>
        <p>Divisés en trois groupes, les participants partent à la rencontre d’acteurs locaux pour observer et échanger sur les bonnes pratiques. Ils sont accompagnés de deux facilitateurs et d’un relai local qui leur font découvrir le territoire, les lieux et les acteurs qui le composent. Chaque itinéraire est jalonné de visites, discussions et analyses de terrain.</p>

        <h4>3. Atterrissage (Genève)</h4>
        <p>Riche d’apprentissages, de découvertes, de questionnements et d’idées, les 3 groupes se retrouvent à Genève. Ils partagent leurs expériences et co-construisent un livrable commun destiné à transmettre les apprentissages. L’occasion de questionner la suite à donner à ce voyage et les modalités de transmission à mettre en place. </p>

      </AppSection>


      <AppSection
              title="Ce qu'il·el﻿les ont produits"
              svg_path="shapes/section_A.mp4"
              uniq_id="section_03"
      >
        <p><a>Questions produites avant le départ</a></p>
        <p><a>Livret de cartes postales</a></p>
        <p><a>Carnet de voyage - Bruxelles</a></p>
        <p><a>Carnet de voyage - Marseille</a></p>
        <p><a>Carnet de voyage - Paris</a></p>
        <p><a>Les défis</a></p>
        <p><a>Les plaidoyers</a></p>

      </AppSection>


      <AppSection
              title="Gallerie photo + 3 video ville"
              svg_path="shapes/section_A.mp4"
              uniq_id="section_02"
      >

        <AppVideo
                video_id="Rz26CazWCe9yPtB"
        />

      </AppSection>

      <AppSection
              title="Participant·e·xs"
              svg_path="shapes/section_A.mp4"
              uniq_id="section_02"
      >
        <p style="text-align: center">Alain Bolle
        <br>Anaïse Antille
        <br>Antonin Calderon
        <br>Arnaud Idelon 
        <br>Arnaud Moreillon
        <br>Aude Bumbacher
        <br>Barbara Tirone
        <br>Benedicte Le Pimpec
        <br>Bertrand Reich
        <br>Caroline Grondahl
        <br>Charles Beer
        <br>Clément Drévo
        <br>Coline Jüngling-Drévo 
        <br>Cécile Roche Boutin 
        <br>Didier Arnoux
        <br>Elsa Buet 
        <br>Eric Devanthéry
        <br>Fabrice Roman
        <br>François Antille
        <br>Frederic Favre
        <br>Fréderic Steinbruchel
        <br>Irene Gilles Lopez
        <br>Isabelle Gattiker
        <br>Joanna Drevard
        <br>Juliette Piat-Martinaud
        <br>Katia Sunier
        <br>Kim Pittier
        <br>Laetitia Mahrer
        <br>Lara Kochnitzky
        <br>Lisa Delapapa
        <br>Marie Weber
        <br>Matthias Lecoq
        <br>Morgane Robert
        <br>Nadia Cao
        <br>Ollivier Gross
        <br>Oscar Bellier
        <br>Quentin Mathieu
        <br>Remy Barbe
        <br>Roman Gampert
        <br>Sacha Kortus
        <br>Simon Gaberell
        <br>Sophie Buchs
        <br>Tarramo Broennimann
        <br>Théodore Turrettini
        <br>Trinité Laroche
        <br>Valérie Spagna
        <br>Yann Boggio</p>
      </AppSection>



    </div>
</template>





<script setup lang="ts">

const timelineContent: {
    title: string,
    date: string
    description: string
}[] = [
    {
        title: 'Entretiens individuels',
        date: 'De juillet à octobre 2024',
        description: 'Interviews',
    },
    {
        title: 'Rencontre',
        date: '13 septembre 2024',
        description: '1er déjeuner et rencontres entre voyageur·euses',
    },
    {
        title: 'Préparation',
        date: '12 novembre 2024',
        description: 'Journée de préparation',
    },
    {
        title: 'Exploration',
        date: '13 au 15 novembre 2024',
        description: 'Départ pour Bruxelles, Paris et Marseille',
    },
    {
        title: 'Atterrissage',
        date: '6 décembre 2024',
        description: 'Mise en commun',
    },
]
</script>





<style lang="scss" scoped >
.v-page-index {
  max-width: 55rem;
  margin: auto;
  border-bottom: solid 1px var(--app-color-beige--dark);
}
</style>
