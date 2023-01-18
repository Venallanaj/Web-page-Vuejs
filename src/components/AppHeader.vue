<template>

  <nav class="navbar navbar-expand-lg navbar-light ">
   <div class="container">
  
    <img src="../assets/brand-logo.png" alt="logo-brand">


     <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
       <span class="navbar-toggler-icon"></span>
     </button>
     <div class="collapse navbar-collapse" id="navbarSupportedContent">
       <ul class="navbar-nav me-auto mb-2 mb-lg-0">
   
       </ul>
       <div class="d-flex  align-items-center">
        <span class="fs-5 fw-bolder me-5 text-navbar"> consectetuer</span>
         <button class="btn btn-outline-success" type="submit">Anmelden</button>
       </div>
     </div>
   </div>
 </nav>
 
 
 </template>
   
   <script>

   export default {
     name: 'AppHeader',
    
   }
   </script>
   
   <!-- Add "scoped" attribute to limit CSS to this component only -->
   <style scoped lang="scss">
 .text-navbar{
  color:#00008B ;
 }
 .btn{

  border: 1px solid #00008B !important;
  color: #00008B !important;
  padding: 12px 28px;
  text-decoration: none;
  display: inline-block;
  font-size: 16px;
  margin: 4px 2px;
  cursor: pointer;
  border-radius: 25px;
 }	
 .btn:hover{
  border: 1px solid #00008B !important;
  background-color: white;
 color: #00008B !important;
 }
   </style>
   