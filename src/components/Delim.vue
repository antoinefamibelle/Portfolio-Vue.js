<template>
  <v-sheet
    style="border-radius:30px"
    elevation="10"
  >
    <div class="separator">
      <v-row class="fill-height" justify="center" style="text-align:center">
        <div class="text">{{ str }}</div>
      </v-row>
    </div>
  </v-sheet>
</template>

<style scoped>
.separator {
  height: 100px;
  color: white;
  background-color: #1976d2;
}

.text {
  font-size: 25px;
  margin-top: 25px;
}

@media only screen and (max-width: 960px) {
  .text{
    font-size: 25px;
    margin-top: 10px;
    color: dark;
  }
}
</style>

<script>
export default {
  name: "Delimitation",
  props: {
    str: String
  }
};
</script>
