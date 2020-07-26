<template>
  <v-sheet
    style="margin-left: 15%; margin-top: -35px; border-radius:30px"
    width="70%"
    elevation="5"
  >
    <div style="background-color:#303030; margin-top: 10px; border-radius:30px;">
      <v-timeline style="width:95%; margin-left:27px" :dense="$vuetify.breakpoint.smAndDown">
        <div class="conditionalBtn" v-if="seeAll === true">
          <v-btn
            class="ma-1"
            outlined
            color="blue"
            @click="seeAll = false;"
          >Afficher uniquement les experiences professionnelles</v-btn>
          <div v-for="item in Exps" :key="item.logo" style="padding-top:20px">
            <v-timeline-item
              fill-dot
              small
              :color="item.color"
              :right="item.right"
              :left="item.left"
            >
              <v-card>
                <v-card-title :class="item.cardColor">
                  <v-icon dark size="42" class="mr-4">{{item.titleIcon}}</v-icon>
                  <h2 class="display-1 white--text font-weight-light">{{ item.name }}</h2>
                </v-card-title>
                <v-container>
                  <v-row>
                    <v-col cols="12" md="10">{{item.description}}</v-col>
                    <v-col class="hidden-sm-and-down text-right" md="2">
                      <v-icon size="45" style="margin-right: 20px; margin-left:-10px">{{item.icon}}</v-icon>
                    </v-col>
                  </v-row>
                </v-container>
              </v-card>
            </v-timeline-item>
          </div>
        </div>
        <div class="conditionalBtn" v-else>
          <v-btn class="ma-1" outlined color="blue" @click="seeAll = true">Tout Afficher</v-btn>
          <div v-for="item in Exps" :key="item.logo" style="padding-top:20px">
            <v-timeline-item
              v-if="item.professionnel === true"
              fill-dot
              small
              :color="item.color"
              :right="item.right"
              :left="item.left"
            >
              <v-card v-if="item.professionnel === true">
                <v-card-title :class="item.cardColor">
                  <v-icon dark size="42" class="mr-4">{{item.titleIcon}}</v-icon>
                  <h2 class="display-1 white--text font-weight-light">{{ item.name }}</h2>
                </v-card-title>
                <v-container>
                  <v-row>
                    <v-col cols="12" md="10">{{item.description}}</v-col>
                    <v-col class="hidden-sm-and-down text-right" md="2">
                      <v-icon size="45" style="margin-right: 20px; margin-left:-10px">{{item.icon}}</v-icon>
                    </v-col>
                  </v-row>
                </v-container>
              </v-card>
            </v-timeline-item>
          </div>
        </div>
      </v-timeline>
    </div>
  </v-sheet>
</template>

<script>
export default {
  name: "XpDesktop",
  data() {
    return {
      seeAll: true,
      Exps: [
        {
          logo:
            "https://www.google.com/url?sa=i&url=https%3A%2F%2Fwww.blog-nouvelles-technologies.fr%2F2312%2Fhtml5-ou-html-la-question-se-pose%2F&psig=AOvVaw2SaUGiuxy1TtXH7KAHefnq&ust=1589414369428000&source=images&cd=vfe&ved=0CAIQjRxqFwoTCIiV7ojEr-kCFQAAAAAdAAAAABAZ",
          name: "Netflix",
          description:
            "Réalisation de l'application Netflix avec un design différent afin d'apprendre les bases de Flutter dans un premier projet",
          color: "#e50914",
          date: "01/05/2020",
          left: true,
          right: false,
          professionnel: false,
          icon: "mdi-cellphone-iphone",
          titleIcon: "mdi-alpha-n-box",
          cardColor: "red"
        },
        {
          logo:
            "https://www.google.com/url?sa=i&url=https%3A%2F%2Fwww.blog-nouvelles-technologies.fr%2F2312%2Fhtml5-ou-html-la-question-se-pose%2F&psig=AOvVaw2SaUGiuxy1TtXH7KAHefnq&ust=1589414369428000&source=images&cd=vfe&ved=0CAIQjRxqFwoTCIiV7ojEr-kCFQAAAAAdAAAAABAZ",
          name: "MyArcade",
          description:
            "Réalisation du Core d'une borne d'arcade en C++. Ce Core doit être capable de gérer les librairies partagées afin de pouvoir faire tourner n'importe quel jeu avec des librairies graphique (SFML / Ncurses / SDL)",
          color: "#64b688",
          date: "12/12/2012",
          left: false,
          right: true,
          professionnel: false,
          icon: "mdi-gamepad-variant-outline",
          cardColor: "grey",
          titleIcon: "mdi-alpha-a-box"
        },
        {
          logo:
            "https://www.google.com/url?sa=i&url=https%3A%2F%2Fwww.blog-nouvelles-technologies.fr%2F2312%2Fhtml5-ou-html-la-question-se-pose%2F&psig=AOvVaw2SaUGiuxy1TtXH7KAHefnq&ust=1589414369428000&source=images&cd=vfe&ved=0CAIQjRxqFwoTCIiV7ojEr-kCFQAAAAAdAAAAABAZ",
          name: "ImageCompressor",
          description:
            "Création d'un logiciel de compression d'image en fonctionnel (HASKELL) avec l'implémentation de l'algorithme le plus optimisé (K-MEANS)",
          color: "#64b688",
          date: "12/12/2012",
          left: true,
          right: false,
          professionnel: false,
          icon: "mdi-image-size-select-large",
          cardColor: "pink",
          titleIcon: "mdi-alpha-i-box"
        },

        {
          logo:
            "https://www.google.com/url?sa=i&url=https%3A%2F%2Fwww.blog-nouvelles-technologies.fr%2F2312%2Fhtml5-ou-html-la-question-se-pose%2F&psig=AOvVaw2SaUGiuxy1TtXH7KAHefnq&ust=1589414369428000&source=images&cd=vfe&ved=0CAIQjRxqFwoTCIiV7ojEr-kCFQAAAAAdAAAAABAZ",
          name: "Akatek-Formateur Vue.js",
          description:
            "Formateur Vue.js auprès d'élèves de 3ème année en développement web en amphithéâtre. Formation en cours. Déjà +15 heures réalisées, un test de validation des acquis et un accompagnement des élèves sur leurs projets.",
          color: "#64b688",
          date: "12/12/2012",
          left: false,
          right: true,
          professionnel: true,
          icon: "mdi-account",
          cardColor: "green",
          titleIcon: "mdi-alpha-a-box"
        },
        {
          logo:
            "https://www.google.com/url?sa=i&url=https%3A%2F%2Fwww.blog-nouvelles-technologies.fr%2F2312%2Fhtml5-ou-html-la-question-se-pose%2F&psig=AOvVaw2SaUGiuxy1TtXH7KAHefnq&ust=1589414369428000&source=images&cd=vfe&ved=0CAIQjRxqFwoTCIiV7ojEr-kCFQAAAAAdAAAAABAZ",
          name: "Developpeur Freelance",
          description:
            "Différentes missions Web (Vue.js / React.js / Angular.js) afin de répondre à différents besoins clients. Autoentrepreneur en développement de site web, en maintenance et formation.",
          color: "#64b688",
          date: "12/12/2012",
          left: true,
          right: false,
          professionnel: true,
          icon: "mdi-laptop",
          cardColor: "blue",
          titleIcon: "mdi-alpha-f-box"
        },
        {
          logo:
            "https://www.google.com/url?sa=i&url=https%3A%2F%2Fwww.blog-nouvelles-technologies.fr%2F2312%2Fhtml5-ou-html-la-question-se-pose%2F&psig=AOvVaw2SaUGiuxy1TtXH7KAHefnq&ust=1589414369428000&source=images&cd=vfe&ved=0CAIQjRxqFwoTCIiV7ojEr-kCFQAAAAAdAAAAABAZ",
          name: "Nike",
          description:
            "Participation à la Project Week 2020 Nike X Epitech. Réalisation d'une application mobile (Swift) afin de proposer une solution innovante à une problématique sociétale moderne.",
          color: "#64b688",
          date: "12/12/2012",
          left: false,
          right: true,
          professionnel: false,
          icon: "mdi-cellphone-iphone",
          cardColor: "pink",
          titleIcon: "mdi-alpha-n-box"
        },
        {
          logo:
            "https://www.google.com/url?sa=i&url=https%3A%2F%2Fwww.blog-nouvelles-technologies.fr%2F2312%2Fhtml5-ou-html-la-question-se-pose%2F&psig=AOvVaw2SaUGiuxy1TtXH7KAHefnq&ust=1589414369428000&source=images&cd=vfe&ved=0CAIQjRxqFwoTCIiV7ojEr-kCFQAAAAAdAAAAABAZ",
          name: "Developpeur Full Stack",
          description:
            "Stage de 6 mois en tant que développeur web Fullstack pour une startup (Spid-Tech) spécialisée dans la création et fourniture de sites web clefs dédiés aux concessionnaires. Technologies utilisées : Vue.js, Node.js, PHP, Mysql, Prestashop.",
          color: "#eb6228",
          date: "12/12/2012",
          left: true,
          right: false,
          professionnel: true,
          icon: "mdi-laptop",
          cardColor: "red",
          titleIcon: "mdi-alpha-s-box"
        },
        {
          logo:
            "https://www.google.com/url?sa=i&url=https%3A%2F%2Fwww.blog-nouvelles-technologies.fr%2F2312%2Fhtml5-ou-html-la-question-se-pose%2F&psig=AOvVaw2SaUGiuxy1TtXH7KAHefnq&ust=1589414369428000&source=images&cd=vfe&ved=0CAIQjRxqFwoTCIiV7ojEr-kCFQAAAAAdAAAAABAZ",
          name: "Dogify",
          description:
            "Réalisation d'une application Mobile (Swift) pour le pôle de recherche d'Epitech Paris afin d'apprendre une nouvelle technologie.",
          color: "#eb6228",
          date: "12/12/2012",
          left: false,
          right: true,
          professionnel: false,
          icon: "mdi-dog",
          cardColor: "blue",
          titleIcon: "mdi-alpha-d-box"
        },
        {
          logo:
            "https://www.google.com/url?sa=i&url=https%3A%2F%2Fwww.blog-nouvelles-technologies.fr%2F2312%2Fhtml5-ou-html-la-question-se-pose%2F&psig=AOvVaw2SaUGiuxy1TtXH7KAHefnq&ust=1589414369428000&source=images&cd=vfe&ved=0CAIQjRxqFwoTCIiV7ojEr-kCFQAAAAAdAAAAABAZ",
          name: "Hackaton",
          description:
            "Hackathon de 24h pour la Sociéte Générale : Création d'un bot de trading en language C.",
          color: "#eb6228",
          date: "12/12/2012",
          left: true,
          right: false,
          professionnel: false,
          icon: "mdi-cash-usd",
          cardColor: "red",
          titleIcon: "mdi-alpha-h-box"
        }
      ]
    };
  }
};
</script>