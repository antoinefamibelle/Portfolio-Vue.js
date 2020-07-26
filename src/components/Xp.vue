<template>
  <div>
    <div class="d-none d-lg-block">
      <XpDesktop />
    </div>
    <div class="d-flex d-sm-flex d-md-flex d-lg-none">
      <XpMobile />
    </div>
  </div>
</template>

<style scoped>
.conditionalBtn {
  margin-bottom: 15px;
}
</style>

<script>
import XpMobile from "./XpMobile";
import XpDesktop from "./XpDesktop";

export default {
  name: "Xp",
  components: {
    XpMobile,
    XpDesktop
  },
};
</script>