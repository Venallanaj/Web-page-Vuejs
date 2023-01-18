<template>
    <div class="container">
      <div class="row mt-5 mb-5">
          <div class="col-lg-12">
              <h5 class="fw-bold">{{ctatitle }}</h5>
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
     
    }
  }
  </script>
  
  <style scoped lang="scss">
  .button{
  background-color: #8FDDDF;
  border: none;
  color: white;
  padding: 15px 32px;
  text-align: center;
  text-decoration: none;
  display: inline-block;
  font-size: 16px;
  border-radius: 25px;
  }
  </style>
  
  
  