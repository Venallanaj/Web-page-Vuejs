<template>
  <div class="container mt-4">
    <div class="row">
      <div class="sliders">
        <button @click="previous()">
          <img src="../assets/prev.png" alt="prev" />
        </button>
        <div
          class="col-lg-4"
          v-for="(review, index) in reviews"
          :key="review.id"
        >
          <card class="card" v-if="index == current">
            <div class="card-body">
              <img :src="image" alt="logo_brand" />
              <img :src="quotation" alt="quotation" />

              <p class="card-text">{{ review.desciption }}</p>
              {{ review.fullName }}
              {{ review.position }}
            </div>
          </card>
        </div>

        <button @click="next()">
          <img src="../assets/next.png" alt="next" />
        </button>
      </div>
    </div>
  </div>
</template>

<script>
import image from "../assets/brand-logo.png";
import quotation from "../assets/shape-qutions.png";

export default {
  name: "AppSlider",
  data: function () {
    return {
      timer: null,
      current: 0,
      reviews: [
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
  methods: {
    previous() {
      this.current =
        Math.abs(this.reviews.length + (this.current - 1)) %
        this.reviews.length;
      console.log(this.current);
    },
    next() {
      //this.current = (this.current + 1) % this.reviews.length;

      this.current++;

      if (this.current >= this.reviews.length) {
        this.current = 0;
      }
    },
    startLoop() {
      this.timer = setInterval(this.next, 2000);
    },
    endLoop() {
      clearInterval(this.timer);
    },
    created() {
      this.startLoop();
    },
    beforeDestroy() {
      this.endLoop();
    },
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
  padding-top: 40px;
  padding-bottom: 30px;
  padding-left: 15px;
  padding-right: 15px;
  font-size: 17px;
}
.card-text {
  text-align: left;
}

.sliders {
  height: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
}
/* Next & previous buttons */
.sliders button {
  border: 0;
}
</style>
