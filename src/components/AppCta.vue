<template>
  <div class="container p-5 mt-5 mb-5">
    <div class="row">
      <div class="col-lg-12">
        <h3 class="fw-bold fs-3 mb-4">{{ ctatitle }}</h3>
        <button class="button">Lorem ipsum</button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "AppTitle",
  props: {
    ctatitle: String,
  },
};
</script>

<style scoped lang="scss">
.button {
  background-color: #63cccf;
  border: none;
  color: white;
  padding: 15px 32px;
  text-align: center;
  font-size: 16px;
  font-weight: bold;
  border-radius: 25px;
}
</style>
