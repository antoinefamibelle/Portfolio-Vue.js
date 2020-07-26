<template>
  <div style="background-color:#303030; height:50vh; overflow:auto;">
    <v-container>
      <v-row>
        <v-col cols="12" md="6">
          <div col="6" style="margin-top:20px">
            <v-progress-circular
              v-for="item in Webs"
              :key="item.name"
              :rotate="-90"
              :size="100"
              :width="15"
              :value="item.level"
              :color="item.color"
              style="margin-left: 15px; margin-top:15px"
            >
              <span>{{ item.name }}</span>
            </v-progress-circular>
          </div>
        </v-col>

        <v-divider class="mx-4" inset vertical />

        <v-col cols="12" md="5">
          <div style="margin-top:40px; margin-left:30px; margin-right:30px">
            <div v-for="item in Mobiles" :key="item.logo" style="margin-top:15px;text-align:center">
              <span class="display-01" style="margin-bottom: -5px; ">{{ item.name }}</span>
              <h1></h1>
              <v-progress-linear
                :value="item.level"
                style="margin-top:5px"
                rounded
                stream
                height="10px"
                buffer-value="0"
              ></v-progress-linear>
            </div>
          </div>
        </v-col>
        <v-col cols="12" md="12">
          <div style="margin-top:60px; margin-left:30px; margin-right:30px">
            <div v-for="item in Others" :key="item.logo" style="margin-top:15px; text-align:center">
              <span class="display-01" style="margin-bottom: -5px;">{{ item.name }} : {{item.score}}</span>
              <h1></h1>
              <v-progress-linear
                :value="item.level"
                style="margin-top:5px"
                rounded
                stream
                stripped="true;"
                height="10px"
                buffer-value="0"
              ></v-progress-linear>
            </div>
          </div>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>



<style scoped>
span {
  color: white;
}
</style>

<script>
export default {
  name: "Test",
  data() {
    return {
      Webs: [
        {
          logo:
            "https://www.google.com/url?sa=i&url=https%3A%2F%2Fwww.blog-nouvelles-technologies.fr%2F2312%2Fhtml5-ou-html-la-question-se-pose%2F&psig=AOvVaw2SaUGiuxy1TtXH7KAHefnq&ust=1589414369428000&source=images&cd=vfe&ved=0CAIQjRxqFwoTCIiV7ojEr-kCFQAAAAAdAAAAABAZ",
          name: "Html",
          level: 90,
          color: "#eb6228"
        },
        {
          logo:
            "https://www.google.com/url?sa=i&url=https%3A%2F%2Fwww.blog-nouvelles-technologies.fr%2F2312%2Fhtml5-ou-html-la-question-se-pose%2F&psig=AOvVaw2SaUGiuxy1TtXH7KAHefnq&ust=1589414369428000&source=images&cd=vfe&ved=0CAIQjRxqFwoTCIiV7ojEr-kCFQAAAAAdAAAAABAZ",
          name: "Css",
          level: 80,
          color: "#3796D0"
        },
        {
          logo:
            "https://www.google.com/url?sa=i&url=https%3A%2F%2Fwww.blog-nouvelles-technologies.fr%2F2312%2Fhtml5-ou-html-la-question-se-pose%2F&psig=AOvVaw2SaUGiuxy1TtXH7KAHefnq&ust=1589414369428000&source=images&cd=vfe&ved=0CAIQjRxqFwoTCIiV7ojEr-kCFQAAAAAdAAAAABAZ",
          name: "Node.js",
          level: 60,
          color: "#74AB61"
        },
        {
          logo:
            "https://www.google.com/url?sa=i&url=https%3A%2F%2Fwww.blog-nouvelles-technologies.fr%2F2312%2Fhtml5-ou-html-la-question-se-pose%2F&psig=AOvVaw2SaUGiuxy1TtXH7KAHefnq&ust=1589414369428000&source=images&cd=vfe&ved=0CAIQjRxqFwoTCIiV7ojEr-kCFQAAAAAdAAAAABAZ",
          name: "Angular.js",
          level: 65,
          color: "#D90032"
        },
        {
          logo:
            "https://www.google.com/url?sa=i&url=https%3A%2F%2Fwww.blog-nouvelles-technologies.fr%2F2312%2Fhtml5-ou-html-la-question-se-pose%2F&psig=AOvVaw2SaUGiuxy1TtXH7KAHefnq&ust=1589414369428000&source=images&cd=vfe&ved=0CAIQjRxqFwoTCIiV7ojEr-kCFQAAAAAdAAAAABAZ",
          name: "React.js",
          level: 50,
          color: "#60D4F7"
        },
        {
          logo:
            "https://www.google.com/url?sa=i&url=https%3A%2F%2Fwww.blog-nouvelles-technologies.fr%2F2312%2Fhtml5-ou-html-la-question-se-pose%2F&psig=AOvVaw2SaUGiuxy1TtXH7KAHefnq&ust=1589414369428000&source=images&cd=vfe&ved=0CAIQjRxqFwoTCIiV7ojEr-kCFQAAAAAdAAAAABAZ",
          name: "Vue.js",
          level: 85,
          color: "#42AE7D"
        },
        {
          logo:
            "https://www.google.com/url?sa=i&url=https%3A%2F%2Fwww.blog-nouvelles-technologies.fr%2F2312%2Fhtml5-ou-html-la-question-se-pose%2F&psig=AOvVaw2SaUGiuxy1TtXH7KAHefnq&ust=1589414369428000&source=images&cd=vfe&ved=0CAIQjRxqFwoTCIiV7ojEr-kCFQAAAAAdAAAAABAZ",
          name: "Boostrap",
          level: 80,
          color: "#6936B2"
        },
        {
          logo:
            "https://www.google.com/url?sa=i&url=https%3A%2F%2Fwww.blog-nouvelles-technologies.fr%2F2312%2Fhtml5-ou-html-la-question-se-pose%2F&psig=AOvVaw2SaUGiuxy1TtXH7KAHefnq&ust=1589414369428000&source=images&cd=vfe&ved=0CAIQjRxqFwoTCIiV7ojEr-kCFQAAAAAdAAAAABAZ",
          name: "Vuetify",
          level: 95,
          color: "#A9D7F8"
        }
      ],
      Mobiles: [
        {
          logo:
            "https://www.google.com/url?sa=i&url=https%3A%2F%2Fwww.blog-nouvelles-technologies.fr%2F2312%2Fhtml5-ou-html-la-question-se-pose%2F&psig=AOvVaw2SaUGiuxy1TtXH7KAHefnq&ust=1589414369428000&source=images&cd=vfe&ved=0CAIQjRxqFwoTCIiV7ojEr-kCFQAAAAAdAAAAABAZ",
          name: "Swift",
          level: 50
        },
        {
          logo:
            "https://www.google.com/url?sa=i&url=https%3A%2F%2Fwww.blog-nouvelles-technologies.fr%2F2312%2Fhtml5-ou-html-la-question-se-pose%2F&psig=AOvVaw2SaUGiuxy1TtXH7KAHefnq&ust=1589414369428000&source=images&cd=vfe&ved=0CAIQjRxqFwoTCIiV7ojEr-kCFQAAAAAdAAAAABAZ",
          name: "Flutter",
          level: 40,
          color: "#D90032"
        },
        {
          logo:
            "https://www.google.com/url?sa=i&url=https%3A%2F%2Fwww.blog-nouvelles-technologies.fr%2F2312%2Fhtml5-ou-html-la-question-se-pose%2F&psig=AOvVaw2SaUGiuxy1TtXH7KAHefnq&ust=1589414369428000&source=images&cd=vfe&ved=0CAIQjRxqFwoTCIiV7ojEr-kCFQAAAAAdAAAAABAZ",
          name: "React Native",
          level: 40,
          color: "#60D4F7"
        },
        {
          logo:
            "https://www.google.com/url?sa=i&url=https%3A%2F%2Fwww.blog-nouvelles-technologies.fr%2F2312%2Fhtml5-ou-html-la-question-se-pose%2F&psig=AOvVaw2SaUGiuxy1TtXH7KAHefnq&ust=1589414369428000&source=images&cd=vfe&ved=0CAIQjRxqFwoTCIiV7ojEr-kCFQAAAAAdAAAAABAZ",
          name: "PWA (Progressive Web App)",
          level: 70,
          color: "#60D4F7"
        }
      ],
      Others: [
        {
          name: "Francais",
          level: 93,
          score: "Langue Maternelle"
        },
        {
          name: "Anglais Toeic",
          level: 85,
          score: 880
        }
      ]
    };
  }
};
</script>