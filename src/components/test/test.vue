<template>

  <v-sheet style="margin-left: 20%; margin-top: -35px; border-radius:30px" width="60%" elevation="5">
    <div style="background-color:#303030; margin-top: 10px; border-radius:30px;">
      <v-timeline style="width:95%; margin-left:27px" :dense="$vuetify.breakpoint.smAndDown">
        <v-timeline-item v-for="item in Exps" :key="item.logo"
          fill-dot 
          small 
          :color="item.color"
          :right="item.right" 
          :left="item.left"
          >
          <v-card>
            <v-card-title 
              :class="item.cardColor"
              >
              <v-icon dark size="42" class="mr-4">mdi-magnify</v-icon>
              <h2 class="display-1 white--text font-weight-light">{{ item.name }}</h2>
            </v-card-title>
            <v-container>
              <v-row>
                <v-col
                  cols="12"
                  md="10"
                >{{item.description}}</v-col>
                <v-col class="hidden-sm-and-down text-right" md="2">
                  <v-icon size="64">{{item.icon}}</v-icon>
                </v-col>
              </v-row>
            </v-container>
          </v-card>
        </v-timeline-item>
      </v-timeline>
      </div>
  </v-sheet>

</template>

<style scoped>
</style>

<script>
export default {
  name: "Test",
  data() {
    return {
      Exps: [
        {
          logo:
            "https://www.google.com/url?sa=i&url=https%3A%2F%2Fwww.blog-nouvelles-technologies.fr%2F2312%2Fhtml5-ou-html-la-question-se-pose%2F&psig=AOvVaw2SaUGiuxy1TtXH7KAHefnq&ust=1589414369428000&source=images&cd=vfe&ved=0CAIQjRxqFwoTCIiV7ojEr-kCFQAAAAAdAAAAABAZ",
          name: "Netflix",
          description: 'Redesign the netflix app',
          color: "#eb6228",
          date: "12/12/2012",
          left: true,
          right: false,
          professionnel: true,
          icon: "mdi-calendar-text",
          cardColor: "red",
        },
        {
          logo:
            "https://www.google.com/url?sa=i&url=https%3A%2F%2Fwww.blog-nouvelles-technologies.fr%2F2312%2Fhtml5-ou-html-la-question-se-pose%2F&psig=AOvVaw2SaUGiuxy1TtXH7KAHefnq&ust=1589414369428000&source=images&cd=vfe&ved=0CAIQjRxqFwoTCIiV7ojEr-kCFQAAAAAdAAAAABAZ",
          name: "html",
          description: 90,
          color: "#eb6228",
          date: "12/12/2012",
          left: false,
          right: true,
          professionnel: true,
          icon: "mdi-calendar-text",
           cardColor: "yellow",
        },
        {
          logo:
            "https://www.google.com/url?sa=i&url=https%3A%2F%2Fwww.blog-nouvelles-technologies.fr%2F2312%2Fhtml5-ou-html-la-question-se-pose%2F&psig=AOvVaw2SaUGiuxy1TtXH7KAHefnq&ust=1589414369428000&source=images&cd=vfe&ved=0CAIQjRxqFwoTCIiV7ojEr-kCFQAAAAAdAAAAABAZ",
          name: "html",
          description: 90,
          color: "#eb6228",
          date: "12/12/2012",
          left: true,
          right: false,
          professionnel: false,
          icon: "mdi-calendar-text",
           cardColor: "red",
        },
        {
          logo:
            "https://www.google.com/url?sa=i&url=https%3A%2F%2Fwww.blog-nouvelles-technologies.fr%2F2312%2Fhtml5-ou-html-la-question-se-pose%2F&psig=AOvVaw2SaUGiuxy1TtXH7KAHefnq&ust=1589414369428000&source=images&cd=vfe&ved=0CAIQjRxqFwoTCIiV7ojEr-kCFQAAAAAdAAAAABAZ",
          name: "html",
          description: 90,
          color: "#eb6228",
          date: "12/12/2012",
          left: false,
          right: true,
          professionnel: true,
          icon: "mdi-calendar-text",
           cardColor: "blue",
        },
        {
          logo:
            "https://www.google.com/url?sa=i&url=https%3A%2F%2Fwww.blog-nouvelles-technologies.fr%2F2312%2Fhtml5-ou-html-la-question-se-pose%2F&psig=AOvVaw2SaUGiuxy1TtXH7KAHefnq&ust=1589414369428000&source=images&cd=vfe&ved=0CAIQjRxqFwoTCIiV7ojEr-kCFQAAAAAdAAAAABAZ",
          name: "html",
          description: 90,
          color: "#eb6228",
          date: "12/12/2012",
          left: true,
          right: false,
          professionnel: false,
          icon: "mdi-calendar-text",
           cardColor: "red",
        },
      ],
    };
  }
};
</script>