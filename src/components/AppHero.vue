<template>
  <div :style="image" class="home-banner" style="max-height: 100vh">
    <div class="container">
      <div class="row">
        <div class="col-lg-12">
          <h3 class="fw-bold text-white text-left">{{ herotitle }}</h3>
        </div>
      </div>
      <div class="row mb-4 mt-4 align-items-center">
        <div class="col-lg-4 mb-3">
          <input
            class="form-control me-2"
            type="search"
            id="searchInput"
            placeholder="lorem ipsum"
            aria-label="Search"
            v-model="textInput"
            v-on:keyup="searchData"
          />
        </div>
        <div class="col-lg-4 mb-3">
          <input
            id="setLocation"
            class="form-control me-2"
            type="text"
            placeholder="lorem ipsum dolor"
            aria-label="Search"
          />
        </div>
        <div class="col-lg-4">
          <button class="button">Lorem ipsum</button>
        </div>
      </div>
      <div class="row mb-4 mt-4">
        <div class="col-lg-12">
          <h4 class="text-uppercase text-white fs-5 fw-bolder">
            {{ subtitle }}
          </h4>
        </div>
      </div>
      <div id="buttonsSearch" class="row mb-4 mt-4">
        <div class="col-lg-3">
          <button class="btn mb-md-10">lorem ipsum</button>
        </div>
        <div class="col-lg-3">
          <button class="btn">lorem ipsum dolor sit amet</button>
        </div>
        <div class="col-lg-3"><button class="btn">consectetuer</button></div>
        <div class="col-lg-3"><button class="btn">lorem ipsum</button></div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "AppHero",
  data() {
    return {
      image: {
        backgroundImage: "url(https://i.postimg.cc/0NbqSxfQ/banner-image.png)",
      },
      textInput: "",
    };
  },
  methods: {
    searchData() {
      debugger;

      let filter, buttons, div, b, i, txtValue;
      filter = this.textInput.toUpperCase();
      buttons = document.getElementById("buttonsSearch");
      div = buttons.getElementsByTagName("div");

      // Loop through all list items, and hide those who don't match the search query
      for (i = 0; i < div.length; i++) {
        b = div[i].getElementsByTagName("button")[0];
        txtValue = b.textContent || a.innerText;
        if (txtValue.toUpperCase().indexOf(filter) > -1) {
          div[i].style.display = "";
        } else {
          div[i].style.display = "none";
        }
      }
    },
  },
  props: {
    herotitle: String,
    subtitle: String,
  },
};
</script>

<style scoped lang="scss">
.home-banner {
  background-size: contain;
  background-repeat: no-repeat;
  width: 100vw;
  height: 100vh;
}

h3 {
  text-align: left;
  max-width: 500px;
}

.form-control {
  border-radius: 0 !important;
  padding: 10px 40px !important;
}

/*General styles, for button */
button {
  border: none;
  text-align: center;
  display: inline-block;
  border-radius: 30px;
  font-size: 16px;
  padding: 10px 40px;
}
.button {
  background-color: #008cba; /* Green */
  color: white;
}

.btn {
  color: white;
  border: 2px solid white;
  text-transform: uppercase;
  height: 40px;
}

#searchInput {
  background-image: url("../assets/icon_search.png");
}
#setLocation {
  background-image: url("../assets/location.png");
}
#searchInput,
#setLocation {
  background-repeat: no-repeat;
  background-position: 10px 12px;
}
::placeholder {
  color: #00008b;
  font-weight: bold;
}

/* Extra small devices (phones, 600px and down) */
@media only screen and (max-width: 600px) {
  .btn {
    margin-bottom: 24px;
    color: #008cba;
    border: 2px solid #008cba;
  }
}
@media only screen and (min-width: 600px) {
  .btn {
    margin-bottom: 24px;
  }
}

/* Extra large devices (large laptops and desktops, 1200px and up) */
@media only screen and (min-width: 1200px) {
  .container {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
  }
}
</style>
