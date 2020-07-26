<template>
  <v-row>
    <v-col cols="12" md="6">
      <v-card
        class="mb-12"
        dark
        max-height="350px"
        style="padding-left:10px; padding-right:10px; padding-top:20px; text-align:center"
      >{{Str}}</v-card>
    </v-col>
    <v-col cols="12" md="6">
      <div class="image-cropper">
        <div class="profile-pic">
          <v-img
            :src="'https://media-exp1.licdn.com/dms/image/C5603AQHUsFa4yPemvw/profile-displayphoto-shrink_200_200/0?e=1594857600&v=beta&t=C7QZLIBgWu4rT0jsrPbFANFg3nyGrT0hMXL1-yq9pvk'"
            aspect-ratio="1"
          ></v-img>
        </div>
      </div>
    </v-col>
  </v-row>
</template>

<style scoped>
.profile-pic {
  display: inline;
  height: 100%;
  border-radius: 50%;
  width: 100%;
  justify-content: center;
}

.image-cropper {
  float: right;
  margin-right: 35%;
  width: 200px;
  height: 200px;
  position: relative;
  overflow: hidden;
  border-radius: 50%;
}
</style>

<script>
export default {
  name: "Stepper",
  props: {
      Str: String,
  }
};
</script>
