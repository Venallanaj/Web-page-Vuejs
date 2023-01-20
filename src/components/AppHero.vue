<template>
  <div class="hero-image position-relative">
    <div
      class="container hero-content position-absolute justify-content-center align-items-center"
    >
      <div class="row">
        <div class="col-lg-12 mb-3">
          <div class="hero-title">
            <h3 class="fw-bold text-white text-lg-left">{{ herotitle }}</h3>
          </div>
        </div>
      </div>
      <div class="row">
        <div class="col-lg-4 mb-3">
          <input
            class="form-control me-2"
            type="text"
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
.hero-image {
  background-image: url("https://i.postimg.cc/0NbqSxfQ/banner-image.png");
  height: 500px;
  background-position: center;
  background-repeat: no-repeat;
  background-size: contain;
  position: relative;
}

.hero-content {
  text-align: center;
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  color: white;
}
/* Extra small devices (phones, 600px and down) */
@media only screen and (max-width: 600px) {
  .hero-image {
    background-position: top;
    background-size: cover;
  }
}

@media only screen and (max-width: 600px) {
  .hero-content {
    top: 82%;
  }
}

.hero-title h3 {
  text-align: left;
  max-width: 500px;
}

/**  styloe secondly row */

input[type="text"] {
  padding: 12px 35px;
  margin: 8px 0;
  border: 1px solid #3838bb;
  border-radius: 0;
}
::placeholder {
  color: #00008b;
  font-weight: bold;
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

.button {
  width: 70%;
  background-color: #008cba;
  color: white;
  padding: 14px 20px;
  margin: 8px 0;
  border: none;
  border-radius: 25px;
  cursor: pointer;
  font-weight: bold;
}

.btn {
  color: white;
  border: 2px solid white !important;
  text-transform: uppercase;
  width: 100%;
  padding: 10px 18px;
  margin: 0 10px;
  border-radius: 25px;
  font-weight: bold;
  height: 40px;
}

/* Styel for mobile */

@media only screen and (max-width: 600px) {
  #buttonsSearch {
    margin-top: 60px;
  }
  .btn {
    color: #008cba;
    border: 2px solid #008cba !important;
    margin-bottom: 15px !important;
  }
}

@media only screen and (max-width: 600px) {
  #buttonsSearch {
    margin-top: 60px !important;
  }
}

/* Medium devices (landscape tablets, 768px and up) */
@media only screen and (max-width: 991px) and (min-width: 601px) {
  .hero-image {
    background-size: cover !important;
  }
  .hero-content {
    top: 77%;
  }
  .btn {
    color: #008cba;
    border: 2px solid #008cba !important;
    margin-bottom: 15px !important;
  }
}

/* Medium devices (landscape tablets, 768px and up) */
// @media only screen and (min-width: 768px) {
//   .hero-image {
//     background-size: cover;
//   }
//   .hero-content {
//     top: 75%;
//   }
// }

// @media only screen and (min-width: 600px) {
//   .btn {
//     margin-bottom: 24px;
//   }
// }

// @media only screen and (min-width: 1200px) {
//   .container {
//     position: absolute;
//     top: 50%;
//     left: 50%;
//     transform: translate(-50%, -50%);
//   }
// }
</style>
