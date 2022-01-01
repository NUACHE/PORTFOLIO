<template>
  <MDBNavbar expand="lg"  container>
    <MDBNavbarBrand href="#" class=".h4">Untitled UI</MDBNavbarBrand>
    <MDBNavbarToggler
      @click="collapse1 = !collapse1"
      target="#navbarSupportedContent"
    ></MDBNavbarToggler>
    <MDBCollapse v-model="collapse1" id="navbarSupportedContent">
      <MDBNavbarNav class="mb-2 mb-lg-0">
        <MDBNavbarItem to="#" >
          Home
        </MDBNavbarItem>
        <MDBNavbarItem href="#"   >
          Dashboard
        </MDBNavbarItem>
         <MDBNavbarItem href="#" >
          Projects
        </MDBNavbarItem>
         <MDBNavbarItem href="#" >
          Tasks
        </MDBNavbarItem>
         <MDBNavbarItem href="#" >
          Reporting
        </MDBNavbarItem>
         <MDBNavbarItem href="#" >
          Designers
        </MDBNavbarItem>
       
      
      </MDBNavbarNav>
      <!-- Search form -->
      <div class="d-flex input-group w-auto">
       <a href="https://www.linkedin.com/in/michael-opoku-98a1221a5/" target="_blank">
         <MDBIcon icon="linkedin" iconStyle="fab" class="p-3" size="lg" />
       </a>
       <a href="https://github.com/NUACHE" target="_blank">
 <MDBIcon icon="github" iconStyle="fab" class="p-3" size="lg" />
       </a>
        
       
      </div>
    </MDBCollapse>
  </MDBNavbar>
</template>

<script>
  import {
 
    MDBNavbar,
    MDBNavbarToggler,
    MDBNavbarBrand,
    MDBNavbarNav,
    MDBNavbarItem,
    MDBCollapse,
    MDBIcon
  
  } from 'mdb-vue-ui-kit';
  import { ref } from 'vue';

  export default {
    components: {
     
      MDBNavbar,
      MDBNavbarToggler,
      MDBNavbarBrand,
      MDBNavbarNav,
      MDBNavbarItem,
      MDBCollapse,
     MDBIcon,
   
    },
    setup() {

      const collapse1 = ref(false);
      const dropdown1 = ref(false);

      return {
        collapse1,
        dropdown1
      }
    }
  };
</script>

<style>
 
  .navbar{
    padding-top: 0px;
    padding-bottom: 0px;
    color: black;
    
  }
  a {
    color: black;
    padding: 0px;
  }
  
</style>