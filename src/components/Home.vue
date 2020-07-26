<template>
  <v-carousel cycle height="100vh" :show-arrows="false" hide-delimiters>
    <v-carousel-item v-for="(slide, i) in slides" :key="i" :src="images[i]">
      <v-sheet :color="colors[i]" height="100%">
          <v-row class="fill-height" justify="center" align="center" cols="12" md="12">
           <div class="display-3" style="text-align: center">{{ slide }}</div>
           </v-row>
            <v-icon size="64px">mdi-arrow-expand-down</v-icon>
      </v-sheet>
         
    </v-carousel-item>

  </v-carousel>
</template>

<style scoped>
@font-face {
  font-family: "myFont";
  src: url("/src/assets/fonts/Montserrat-MediumItalic.ttf");
}

.img-text {
  color: white;
}
</style>

<script>
export default {
  name: "Home",

  data() {
    return {
      images: [
        "https://images.unsplash.com/photo-1521185496955-15097b20c5fe?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=2447&q=80",
        "https://images.unsplash.com/photo-1509966756634-9c23dd6e6815?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1610&q=80",
        "https://images.unsplash.com/photo-1562907550-096d3bf9b25c?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1350&q=80"
      ],
      slides: ["Développeur Mobile", "Développeur Web", "Passionné"],
      colors: ["transparent", "transparent", "transparent"]
    };
  }
};
</script>
