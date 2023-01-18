<template>

<!-- Footer -->
<footer class="section-footer">
  <!-- Grid container -->
  <div class="container ">

   <div class="row mb-4 mt-4 d-flex align-items-center">
      <div class="col-lg-1 ">
         <img src="../assets/contact-number.svg" alt=" contact-number">        
     </div>

     <div class="col-lg-1">
        <div class="contact-phone contacts">
            <p class="pt-3"> 
                <a href="tel:+49 12345678000" class="text-white">+49(0)12345678000</a>
            </p>
        </div>

      </div>
        <div class="col-lg-1"></div>

      <div class="col-lg-1 ">
        <img src="../assets/contact-email.svg" alt=" contact-email "> 
        ​ 
     </div>
     <div class="col-lg-1">
        <div class="contact-email contacts">
          <p class="pt-3">  
            <a href = "mailto: info@loremi@com" class="text-white">info@loremipsum@com</a>
          </p>
        </div>
      </div>       
   </div>

    <!--Grid row-->
    <div class="row">
      <!--Grid column-->
      <div class="col-lg-4 col-md-6 mb-4 ">
        <h5 class=" fs-5 fw-bolder">Vivamus</h5>

        <ul class="list-unstyled ">
          <li class="mb-2">
            <a href="#" class="text-white">quam</a>
          </li>
          <li class="mb-2">
            <a href="#" class="text-white">venenatis</a>
          </li>
          <li class="mb-2">
            <a href="#" class="text-white">tincidunt</a>
          </li>
          <li class="mb-2">
            <a href="#" class="text-white">faucibus</a>
          </li>
        </ul>
      </div>
      <!--Grid column-->

      <!--Grid column-->
      <div class="col-lg-4 col-md-6 mb-4 mb-md-0">
        <h5 class="fs-5 fw-bolder">Elementum</h5>

        <ul class="list-unstyled">
            <li class="mb-2">
            <a href="#!" class="text-white text-uppercase">The lorem ipsum</a>
          </li>
          <li class="mb-2">
            <a href="#" class="text-white text-uppercase">Reply</a>
          </li>
         
        </ul>
      </div>
      <!--Grid column-->

      <!--Grid column-->
      <div class="col-lg-4 col-md-6 mb-4 mb-md-0">
        <h5 class="text-uppercase fs-5 fw-bolder"></h5>

        <ul class="list-unstyled mb-0">
            <li class="mb-2 mt-5">
            <a href="#" class="text-white">Datenschutz</a>
          </li>
          <li class="mb-2">
            <a href="#" class="text-white">Impressum</a>
          </li>
          <li class="mb-2">
            <a href="#" class="text-white">Cookie Richtlinien</a>
          </li>
          <li class="mb-2">
            <a href="#" class="text-white">Allgemeine</a>
          </li>
          <li class="mb-2">
            <a href="#" class="text-white">Geschaftsbedingungen</a>
          </li>
        </ul>
      </div>
      <!--Grid column-->

 
    </div>
    <!--Grid row-->
  </div>
  <!-- Grid container -->

  <!-- Copyright -->
  
    <div class="row mb-4 mt-4">
      <div class="col-lg-6">
          <p class="text-white text-copyright">   Copyright© 2021  All right reserved</p>
      </div>
      <div class="col-lg-6"></div>

    </div>
   <!-- Copyright -->
  </footer>
</template>

    <script>
    export default {
      name: 'AppFooter',

    }
    </script>

    <!-- Add "scoped" attribute to limit CSS to this component only -->
    <style scoped lang="scss">
.section-footer{
  padding-top: 50px;
  padding-bottom: 50px;
  background-color: #00008B;
}

 h5{
  padding-left: 3px;
  margin-bottom: 20px;
  color: white;
  letter-spacing: 2px;
 }

  ul li a {
  text-decoration: none;
  }

   .contacts p a {
   text-decoration: none;
   font-size: 17px;
   font-weight: 400;

  }

  /* Use media query for Extra large devices (large laptops and desktops, 1200px and up) */ 
    @media only screen and (min-width: 1200px)  {
    .text-copyright{
    margin-left: -99px
   }  
   h5, ul{
    text-align: left;
   }
   .contacts p{
     margin-left:-30px
   }
}
   


    </style>
