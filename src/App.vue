<template>
  <div>
    <meta
      name="viewport"
      content="width=device-width, initial-scale=1, maximum-scale=1, user-scalable=no, minimal-ui"
    />
    <v-app style="overflow-x: hidden">
      <div>
        <Navbar/>
        <button type="button" class="btn btn-primary">Primary</button>
        <Home id="home" />
         <Delimitation id="me" str="Apprendre à me connaitre en 3 étapes" />
        <Me />
        <Delimitation id="skill" str="Mes compétences" />
        <Skills />
        <Delimitation id="xp" str="Mes experiences" />
        <Xp />
      </div>
    </v-app>
  </div>
</template>

<script>
import Home from "./components/Home";
import Delimitation from "./components/Delim";
import Me from "./components/Me";
import Skills from "./components/Skills";
import Xp from "./components/Xp";
import Navbar from "./components/Navbar";

export default {
  name: "App",

  components: {
    Home,
    Delimitation,
    Me,
    Skills,
    Xp,
    Navbar
  },

  data: () => ({
    //
  })
};
</script>
