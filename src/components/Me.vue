<template>
  <div>
    <div style="overflow:auto width: 100%">
      <v-stepper style="height: 100%" dark v-model="el">
        <v-stepper-header>
          <v-stepper-step :complete="el > 1" step="1">Qui suis-je ?</v-stepper-step>

          <v-divider></v-divider>

          <v-stepper-step :complete="el > 2" step="2">Mes objectifs</v-stepper-step>

          <v-divider></v-divider>

          <v-stepper-step step="3">Mes projets en cours</v-stepper-step>
        </v-stepper-header>

        <div class="d-none d-lg-block" align="center">
          <v-row>
            <v-col v-for="item in Description" :key="item.title" step="item.number" md="6">
              <v-sheet
                height="300px"
                width="750px"
                style="padding-left:75px; padding-right:75px; display:flex; border-radius:30px"
                justify="center"
                align="center"
              >
                <v-card
                  light
                  shaped
                  style="padding: 10px; margin: auto;"
                  align="center"
                  justify="center"
                >{{item.title}}</v-card>
              </v-sheet>
            </v-col>
          </v-row>
        </div>

        <div class="d-flex d-sm-flex d-md-flex d-lg-none" align="center">
          <div class="col-md-6">
            <v-row>
              <v-col md="6">
                <v-sheet
                  height="550px"
                  width="350px"
                  style="padding-left:75px; padding-right:75px;padding-top:25px; padding-bottom: 25px; margin-bottom: 25px; border-radius:30px;display:flex"
                >
                  <v-card
                    light
                    shaped
                    style="padding: 10px; margin: auto;"
                    align="center"
                    justify="center"
                  >{{titleOne}}</v-card>
                </v-sheet>
              </v-col>
            </v-row>
            <v-row>
              <v-col md="6">
                <v-sheet
                  height="550px"
                  width="350px"
                  style="padding: 25px 25px 25px 25px;margin-bottom: 25px; display:flex;border-radius:30px"
                >
                  <v-card
                    light
                    shaped
                    style="padding: 10px; margin: auto;"
                    align="center"
                    justify="center"
                  >{{titleTwo}}</v-card>
                </v-sheet>
              </v-col>
            </v-row>
          </div>
        </div>
      </v-stepper>
    </div>
  </div>
</template>


<style scoped>
.center-div {
  margin: 0 auto;
  width: 100%;
  height: 100vh;
}
</style>

<script>
export default {
  name: "Me",
  data() {
    return {
      projects: [
        {
          name:
            "- une application de Flutter ou je redesign la celebre application Netflix (Flutter) [Projet Perso]"
        },
        {
          name: " - Un jeu Bomberman en réseaux (C++) [Projet Epitech],"
        },
        {
          name:
            "- Un site de redesign de Amazon (React.js / Angular.js) [Projet Perso]"
        }
      ],
      el: 1,
      Description: [
        {
          title: "Bonjour, je m'appelle Antoine Famibelle et je suis actuellement en fin de 2ème année à Epitech Paris. Passionné d'informatique mais aussi sportif de haut niveau, je suis toujours prêt à relever de nouveaux challenges. Les défis sont l'essence même de mon attrait pour l'informatique. Je suis dynamique et très créatif, c'est pourquoi j'aime sentir que je peux me rendre utile dans une entreprise que ce soit du côté du développement que du côté conseil.",
          number: 1
        },
        {
          title:"Passionné d'informatique j'ai beaucoup de projets personnels que je développe en dehors de l'école. C'est à travers l'un d'eux que je me suis découvert un interêt prononcé pour le développement Mobile (Swift / Flutter) mais aussi pour le développement Web (Front-end / Fullstack). Fort d'une expérience de 6 mois en tant que développeur Fullstack dans une start-up et de plusieurs mission en tant qu'indépendant, je suis actuellement à la recherche d'un stage à temps partiel d'octobre 2020 à mars 2021 ainsi que d'un stage à temps plein de mars 2021 à juillet 2021. Idéalement ces stages seraient en Mobile ou en Web cependant je reste à l'écoute de toute autre proposition !",
          number: 2
        }
      ],
      titleOne: "Bonjour, je m'appelle Antoine Famibelle et je suis actuellement en fin de 2ème année à Epitech Paris. Passionné d'informatique mais aussi sportif de haut niveau, je suis toujours prêt à relever de nouveaux challenges. Les défis sont l'essence même de mon attrait pour l'informatique. Je suis dynamique et très créatif, c'est pourquoi j'aime sentir que je peux me rendre utile dans une entreprise que ce soit du côté du développement que du côté conseil.",
      titleTwo: "Passionné d'informatique j'ai beaucoup de projets personnels que je développe en dehors de l'école. C'est à travers l'un d'eux que je me suis découvert un interêt prononcé pour le développement Mobile (Swift / Flutter) mais aussi pour le développement Web (Front-end / Fullstack). Fort d'une expérience de 6 mois en tant que développeur Fullstack dans une start-up et de plusieurs mission en tant qu'indépendant, je suis actuellement à la recherche d'un stage à temps partiel d'octobre 2020 à mars 2021 ainsi que d'un stage à temps plein de mars 2021 à juillet 2021. Idéalement ces stages seraient en Mobile ou en Web cependant je reste à l'écoute de toute autre proposition !",
        
        };
  }
};
</script>