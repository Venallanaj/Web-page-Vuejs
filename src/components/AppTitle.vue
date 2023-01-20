<template>
  <div :style="image" class="banner-review">
    <div class="container">
      <div
        class="row d-flex align-items-center justify-content-center mt-5 mb-5 box-content"
      >
        <div class="col-lg-2">
          <img src="../assets/shape-reviwe.png" alt=" contact-email " />
        </div>
        <div class="col-md-5">
          <h2 class="fw-bold fs-4">{{ title }}</h2>
          <p class="fw-bolder">{{ paragraph }}</p>
        </div>
      </div>
      <AppSlider />
    </div>
  </div>
</template>

<script>
import AppSlider from "./AppSlider.vue";
export default {
  name: "AppTitle",
  components: {
    AppSlider,
  },
  props: {
    title: String,
    paragraph: String,
  },
  data() {
    return {
      image: {
        backgroundImage: "url(https://i.postimg.cc/vHk3CYt5/banner-review.png)",
      },
    };
  },
};
</script>

<style scoped lang="scss">
.banner-review {
  background-size: contain;
  background-repeat: no-repeat;
  width: 100vw;
  // height: 100vh;
  position: relative;
}
/* Extra small devices (phones, 600px and down) */
@media only screen and (max-width: 600px) {
  .banner-review {
    margin-top: 250px;
  }
}
@media only screen and (max-width: 991px) and (min-width: 601px) {
  .box-content {
    margin-top: 200px !important;
  }
}
</style>
