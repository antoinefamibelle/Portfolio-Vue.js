<template>
  <div>
    <div class="d-none d-lg-block">
      <v-bottom-navigation v-model="bottomNav" dark horizontal max-height="50px">
        <v-tabs center-active centered>
          <v-tab>
            <v-btn href="/">Home</v-btn>
          </v-tab>
          <v-tab>
            <v-btn href="#me">Qui suis-je</v-btn>
          </v-tab>
          <v-tab>
            <v-btn href="#skill">Compétences</v-btn>
          </v-tab>
          <v-tab>
            <v-btn href="#xp">Expériences</v-btn>
          </v-tab>
          <v-tab>
            <v-btn href>Contact</v-btn>
          </v-tab>
        </v-tabs>
      </v-bottom-navigation>
    </div>
    <div class="d-flex d-sm-flex d-md-flex d-lg-none" style="background-color:#1E1E1E;">
      <v-row>
        <v-col cols="12">
          <div class="text-center" justify-center>
            <v-btn color="blue" @click="overlay = !overlay">Menu</v-btn>
            <v-overlay :value="overlay">
              <v-row>
                <v-btn icon @click="overlay = false" href="#me">
                  <h3>Qui suis-je ?</h3>
                </v-btn>
              </v-row>
              <v-row>
                <v-btn icon @click="overlay = false" href="#skill">
                  <h3>Competences</h3>
                </v-btn>
              </v-row>
              <v-row>
                <v-btn icon @click="overlay = false" href="#xp">
                  <h3>Experiences</h3>
                </v-btn>
              </v-row>
              <v-row>
                <v-btn icon @click="overlay = false">
                  <h3>Contact</h3>
                </v-btn>
              </v-row>
              <v-row>
                <v-icon>mdi-close</v-icon>
              </v-row>
            </v-overlay>
          </div>
        </v-col>
      </v-row>
    </div>
  </div>
</template>

<style scoped>
v-btn {
  padding-top: "10px";
}
</style>

<script>
export default {
  name: "NavBar",
  data() {
    return {
      overlay: false
    };
  }
};
</script>

