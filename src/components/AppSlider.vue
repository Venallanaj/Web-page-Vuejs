<template>
  <Carousel :settings="settings" :breakpoints="breakpoints">
    <slide v-for="item in items" :key="item.id">
      <div class="carousel__item">
        <card class="card">
          <img :src="image" alt="logo_brand" class="logo_brand" />
          <img :src="quotation" alt="quotation_mark" class="quotation_mark" />
          <div class="card-body">
            {{ item.desciption }}
            {{ item.fullName }}
            {{ item.position }}
          </div>
        </card>
      </div>
    </slide>

    <template #addons>
      <navigation />
      <pagination />
    </template>
  </Carousel>
</template>

<script>
// If you are using PurgeCSS, make sure to whitelist the carousel CSS classes
import "vue3-carousel/dist/carousel.css";
import { Carousel, Slide, Pagination, Navigation } from "vue3-carousel";

import image from "../assets/brand-logo.png";
import quotation from "../assets/shape-qutions.png";

export default {
  name: "AppSlider",
  components: {
    Pagination,
    Carousel,
    Slide,
    Navigation,
  },
  data: function () {
    return {
      items: [
        {
          id: 1,
          desciption:
            "Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aenean commodo ligula eget dolor. Aenean massa. Cum sociis natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus. Donec quam felis, ultricies nec, pellentesque eu, pretium quis, sem. Nulla consequat massa quis enim. ",
          fullName: "Max Mustermann",
          position: "Aenean vulputate (AB), Maecenas ",
        },
        {
          id: 2,
          desciption:
            "222Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aenean commodo ligula eget dolor. Aenean massa. Cum sociis natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus. Donec quam felis, ultricies nec, pellentesque eu, pretium quis, sem. Nulla consequat massa quis enim. ",
          fullName: "Max Mustermann",
          position: "Aenean vulputate (AB), Maecenas ",
        },
        {
          id: 3,

          desciption:
            "22266Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aenean commodo ligula eget dolor. Aenean massa. Cum sociis natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus. Donec quam felis, ultricies nec, pellentesque eu, pretium quis, sem. Nulla consequat massa quis enim. ",
          fullName: "Max Mustermann",
          position: "Aenean vulputate (AB), Maecenas ",
        },
      ],
      image: image,
      quotation: quotation,
    };
  },
};
</script>

<style scoped lang="scss">
.card {
  background-color: white;
  box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2);
  transition: 0.3s;
  width: 100%;
  border: none;
  padding-top: 90px;
  padding-bottom: 5px;
  padding-left: 35px;
  padding-right: 35px;
  font-size: 18px;
  text-align: left;
  position: relative;

  & .logo_brand {
    position: absolute;
    top: 20px;
    left: 16px;
    width: 60px;
    height: auto;
  }
  & .quotation_mark {
    position: absolute;
    left: 10px;
    width: 30px;
    height: auto;
  }
}
</style>
