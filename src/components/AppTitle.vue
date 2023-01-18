<template>
  <div :style="image" class="banner-review" style="max-height: 100vh;">
    <div class="container">
    <div class="row d-flex align-items-center justify-content-center">
      <div class="col-lg-2">
        <img src="../assets/shape-reviwe.png" alt=" contact-email "> 

      </div>
      <div class=" col-md-5 ">
          <h4 class="fw-bold">{{title }}</h4>
          <p class="text-black" >{{ paragraph }}</p>  
      </div>
    </div>
    <AppSlider />
  </div>
</div>  
</template>



<script>
import AppSlider from './AppSlider.vue';
export default {
    name: "AppTitle",
    components: {
      AppSlider
    },
    props: {
    title: String,
    paragraph: String, 
  },
  data(){
     return{
      image: { backgroundImage: "url(https://i.postimg.cc/vHk3CYt5/banner-review.png)" }      
     };
    },
}


</script>

<style scoped lang="scss">
.banner-review{
    background-size: contain; 
    background-repeat: no-repeat;
    width: 100vw; 
    height: 100vh;
}
</style>

