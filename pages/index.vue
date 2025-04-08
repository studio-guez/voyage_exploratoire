<template>
    <div
        class="v-page-index"
    >
      <AppHeader/>


      <AppSection
              title="En bref"
              transform_translate_x ="50%"
              transform_translate_y ="70%"
              transform_scale       ="10"
      >
        <p>En 2024, plus de <strong>35 professionnel·les genevois·es aux profils variés</strong> (travailleurs sociaux, architectes, urbanistes, institutions, fondations, gestionnaires de lieux sociaux) participent à ce 1er voyage exploratoire.</p>
        <p>Ce <strong>voyage immersif</strong> à travers la francophonie, part de Genève pour <strong>découvrir des espaces communs qui soutiennent le changement de dynamique sociale</strong> de notre société.</p>
        <p>À leur retour, l’objectif est d’inspirer la création et la transformation de lieux et projets ayant un impact social et culturel grâce aux apprentissages acquis. Le programme est conçu selon les <strong>besoins</strong> et <strong>questionnements</strong> de chacun des participant·es.</p>
        <p>L’équipe des fantastiques communs rencontre chaque participant·e individuellement, autour d’un entretien, qui permettra de faire émerger les axes du voyage. <strong>Pendant trois jours, les 35 participant·es partent dans 3 villes différentes (Paris, Bruxelles, Marseille) pour rencontrer des porteurs de projets inspirants et analyser les dynamiques locales.</strong></p>
        <p>Le voyage repose sur l’<strong>immersion</strong>, le <strong>partage de savoirs</strong>, la <strong>co-construction</strong> et l’<strong>expérimentation</strong>. Pour qu’il réponde aux enjeux du territoire, il est élaboré avec des acteurs déjà engagés dans ces réflexions et expérimentations.</p>
      </AppSection>





      <AppSection
              title="Documentation du voyage"
              transform_translate_x ="20%"
              transform_translate_y ="220%"
              transform_scale       ="7"
      >

        <p>Production collective en CC-BY-SA initiée par les fantastiques communs dans le cadre d’un voyage exploratoire d’une équipe genevoise pluridisciplinaire à Paris, Bruxelles ou Marseille en Novembre 2024.</p>

        <div class="app-flex">
          <div class="app-flex__col-12">
            <AppFileLink
                    title="Les questions thématiques"
                    description="Ces questions ont été formulées par les voyageur·euses en amont du voyage et ont guidées les interactions avec les intervenant·es."
                    project_directory_name="questionnements"
            />
          </div>
          <div class="app-flex__col-12">
            <AppFileLink
                    title="Livret de cartes postales"
                    description="Ces cartes postales, adressées à Genève, ont été produites recto-verso par les voyageur·euses, à la suite de chaque visite de lieux."
                    project_directory_name="cartes_postales"
            />
          </div>
          <div class="app-flex__col-12">
            <AppFileLink
                    title="Carnet de voyage - Bruxelles"
                    description="Ce carnet a été fourni aux voyageur·euses au départ du train, puis enrichi de leurs apprentissages sur place."
                    project_directory_name="livret-bruxelles"
            />
          </div>
          <div class="app-flex__col-12">
            <AppFileLink
                    title="Carnet de voyage - Marseille"
                    description="Ce carnet a été fourni aux voyageur·euses au départ du train, puis enrichi de leurs apprentissages sur place."
                    project_directory_name="livret-marseille"
            />
          </div>
          <div class="app-flex__col-12">
            <AppFileLink
                    title="Carnet de voyage - Paris"
                    description="Ce carnet a été fourni aux voyageur·euses au départ du train, puis enrichi de leurs apprentissages sur place."
                    project_directory_name="livret-paris"
            />
          </div>
          <div class="app-flex__col-12">
            <AppFileLink
                    title="Les défis"
                    description="Au retour du voyage, les voyageur·euses ont formulé 8 défis à relever par les acteurs genevois pour avoir un plus fort impact social sur le territoire. "
                    project_directory_name="defis"
            />
          </div>
          <div class="app-flex__col-12">
            <AppFileLink
                    title="Les plaidoyers"
                    description="Riche de leurs apprentissages, les voyageur·euses se rassemblent autour de 2 plaidoyers qu’ils ont écrit collectivement : un appel à l’audace et à l’action."
                    project_directory_name="plaidoyers"
            />
          </div>
        </div>


      </AppSection>



      <AppSection
              transform_translate_x ="20%"
              transform_translate_y ="-120%"
              transform_scale       ="6"
      >
        <div style="margin-bottom: var(--app-gutter)">
          <app-gallery
                  directory_name="bruxelles"
                  :image_number="56"
          />
        </div>
        <div style="margin-bottom: var(--app-gutter)">
          <app-gallery
                  directory_name="marseille"
                  :image_number="105"
          />
        </div>
        <div style="margin-bottom: var(--app-gutter)">
          <app-gallery
                  directory_name="paris"
                  :image_number="101"
          />
        </div>
      </AppSection>





      <AppSection
              transform_translate_x ="20%"
              transform_translate_y ="-120%"
              transform_scale       ="6"
              title="Un dispositif en﻿ plusieurs phases"
      >
        <app-timeline
                :items="timelineContent"
        />
      </AppSection>











      <AppSection
              transform_translate_x ="-280%"
              transform_translate_y ="-190%"
              transform_scale       ="8"
              title="Contributeur·ices"
      >
        <div class="v-app-index__contributors">
          <a href="https://www.linkedin.com/in/alain-bolle-41668721/"                 >Alain Bolle</a>
          <span                                                                       >Anaïse Antille</span>
          <a href="https://www.linkedin.com/in/antonin-calderon-43148513b/"           >Antonin Calderon</a>
          <a href="https://www.linkedin.com/in/arnaud-idelon-29b69486/"               >Arnaud Idelon</a>
          <a href="https://www.linkedin.com/in/arnaud-moreillon-6302b235/"            >Arnaud Moreillon</a>
          <a href="https://www.linkedin.com/in/aude-bumbacher-15984817/"              >Aude Bumbacher</a>
          <a href="https://www.linkedin.com/in/barbaratirone/"                        >Barbara Tirone</a>
          <a href="https://www.linkedin.com/in/bénédicte-le-pimpec-8065ab238/"        >Benedicte Le Pimpec</a>
          <a href="https://www.linkedin.com/in/bertrand-r-reich-1611876/"             >Bertrand Reich</a>
          <a href="https://www.linkedin.com/in/caroline-grondahl-b84525116/"          >Caroline Grondahl</a>
          <a href="https://www.linkedin.com/in/cecile-roche-boutin-80993a22/"         >Cécile Roche Boutin</a>
          <a href="https://www.linkedin.com/in/charles-beer-b0345193/"                >Charles Beer</a>
          <a href="https://www.linkedin.com/in/clement-drevo/"                        >Clément Drévo</a>
          <a href="https://www.linkedin.com/in/colinedrevo/"                          >Coline Jüngling-Drévo</a>
          <span                                                                       >Didier Arnoux</span>
          <a href="https://www.linkedin.com/in/elsa-buet-bb98b996/"                   >Elsa Buet</a>
          <a href="https://www.linkedin.com/in/eric-devanthéry-4047b7234/"            >Eric Devanthéry</a>
          <span                                                                       >Fabrice Roman</span>
          <a href="https://www.linkedin.com/in/francoisantille/"                      >François Antille</a>
          <a href="https://www.linkedin.com/in/frédéric-favre-2a97b1181/"             >Frederic Favre</a>
          <a href="https://www.linkedin.com/in/frédéric-steinbrüchel-6937512a2/"      >Fréderic Steinbruchel</a>
          <a href="https://www.linkedin.com/in/irene-gil-lopez-37aa532b/"             >Irene Gilles Lopez</a>
          <a href="https://www.linkedin.com/in/isabellegattiker/"                     >Isabelle Gattiker</a>
          <a href="https://www.linkedin.com/in/joanna-drevard/"                       >Joanna Drevard</a>
          <a href="https://www.linkedin.com/in/juliettepiatmartinaud/"                >Juliette Piat-Martinaud</a>
          <a href="https://www.linkedin.com/in/katia-sunier-2a129419b/"               >Katia Sunier</a>
          <a href="https://www.linkedin.com/in/kim-pittier-a088b8ba/"                 >Kim Pittier</a>
          <a href="https://www.linkedin.com/in/laetitia-mahrer-a9b8316b/"             >Laetitia Mahrer</a>
          <a href="https://www.linkedin.com/in/lara-kochnitzky/"                      >Lara Kochnitzky</a>
          <a href="https://www.linkedin.com/in/lisa-del-papa-a2082430a/"              >Lisa Delapapa</a>
          <a href="https://www.linkedin.com/in/marie-weber-ab5aa1128/"                >Marie Weber</a>
          <a href="https://www.linkedin.com/in/matthias-lecoq-geneva/"                >Matthias Lecoq</a>
          <a href="https://www.linkedin.com/in/morgane-robert-3b733556/"              >Morgane Robert</a>
          <a href="https://www.linkedin.com/in/nadiacao/"                             >Nadia Cao</a>
          <a href="https://www.linkedin.com/in/olliviergross/"                        >Ollivier Gross</a>
          <a href="https://www.linkedin.com/in/oscarbellier/"                         >Oscar Bellier</a>
          <a href="https://www.linkedin.com/in/qmathieu/"                             >Quentin Mathieu</a>
          <a href="https://www.linkedin.com/in/remy-barbe-geneve/"                    >Remy Barbe</a>
          <a href="https://www.linkedin.com/in/roman-gampert-5537b9126/"              >Roman Gampert</a>
          <a href="https://www.linkedin.com/in/alexandar-kortus-18552b5/"             >Sacha Kortus</a>
          <a href="https://www.linkedin.com/in/simon-gaberell-590878201/"             >Simon Gaberell</a>
          <a href="https://www.linkedin.com/in/sophie-buchs-a9595272/"                >Sophie Buchs</a>
          <a href="https://www.linkedin.com/in/tarramo-broennimann-179603239/"        >Tarramo Broennimann</a>
          <a href="https://www.linkedin.com/in/théodore-turrettini-862551162/"        >Théodore Turrettini</a>
          <a href="https://www.linkedin.com/in/trinitelaroche/"                       >Trinité Laroche</a>
          <a href="https://www.linkedin.com/in/valérie-spagna-65977b89/"              >Valérie Spagna</a>
          <a href="https://www.linkedin.com/in/yann-boggio-77770315/"                 >Yann Boggio</a>
        </div>
      </AppSection>

      <AppSection
              transform_translate_x ="-600%"
              transform_translate_y ="150%"
              transform_scale       ="12"
              title="Retour en vidéos"
      >
        <div class="app-index-video__container">
          <AppVideo
                  video_id="92zYTrC2G9jDZAq"
          />
        </div>
        <div class="app-index-video__container">
          <AppVideo
                  video_id="Ew2yfiFfGsKA6oo"
          />
        </div>
        <div class="app-index-video__container">
          <AppVideo
                  video_id="o5xSGcWxzxXapDr"
          />
        </div>
      </AppSection>



    </div>
</template>





<script setup lang="ts">

import AppFileLink from "~/components/AppFileLink.vue";

const timelineContent: {
    title: string,
    date: string
    subtitle: string
    description?: string
}[] = [
    {
        title: 'Entretiens individuels',
        date: 'De juillet à octobre 2024',
        subtitle: 'Interviews',
    },
    {
        title: 'Première rencontre',
        date: '13 septembre 2024',
        subtitle: '1er déjeuner et rencontres entre voyageur·euses',
    },
    {
        title: 'Embarquement des voyageur·euse',
        date: '12 novembre 2024',
        subtitle: 'Journée de préparation',
        description: `
        <p>Avant le départ, les participants se retrouvent pour :</p>
        <ul>
          <li>Se familiariser avec les concepts et outils d’analyse</li>
          <li>Définir les axes de documentation</li>
          <li>Préparer leur parcours</li>
        </ul>
        `
    },
    {
        title: 'Exploration',
        date: '13 au 15 novembre 2024',
        subtitle: 'Départ pour Bruxelles, Paris et Marseille',
        description: `
        <p>Divisés en trois groupes, les participants partent à la rencontre d’acteurs locaux pour observer et échanger sur les bonnes pratiques. Ils sont accompagnés de deux facilitateurs et d’un relai local qui leur font découvrir le territoire, les lieux et les acteurs qui le composent. Chaque itinéraire est jalonné de visites, discussions et analyses de terrain.</p>
        `
    },
    {
        title: 'Atterrissage',
        date: '6 décembre 2024',
        subtitle: 'Mise en commun',
        description: `
        <p>Riche d’apprentissages, de découvertes, de questionnements et d’idées, les 3 groupes se retrouvent à Genève. Ils partagent leurs expériences et co-construisent un livrable commun destiné à transmettre les apprentissages. L’occasion de questionner la suite à donner à ce voyage et les modalités de transmission à mettre en place.</p>
        `
    },
]
</script>





<style lang="scss" scoped >
.v-page-index {
  background: var(--app-color-beige);
  max-width: 55rem;
  margin: auto;
  border-bottom: solid 1px var(--app-color-beige--dark);
}

.app-index-video__container + .app-index-video__container {
  margin-top: 1rem;
}

:global(.v-app-index__contributors) {
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  column-gap: 1rem;
}

:global(.v-app-index__contributors > *) {
  color: inherit;
}
</style>
