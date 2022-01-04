<template>
  <MDBRow style="padding-left: 25px; padding-right: 25px">
    <MDBCol col="3">Contact</MDBCol>
    <MDBCol col="9" style="display: flex; flex-wrap: wrap;" >
    <a :href="contact.link" v-for="contact in contacts" :key="contact.link" >
      <div class="bg-image"  v-bind:style="{ 'background-image': 'url(' + contact.image  + ')' }">
         
          </div>
      </a> 
     
         
    </MDBCol>
  
  
  </MDBRow>
</template>

<script>
import {  MDBCol, MDBRow } from "mdb-vue-ui-kit";

export default {
   components: {
  MDBCol, MDBRow, 
  },
  data() {
  return {
    contacts : [
    {
      link : "https://www.linkedin.com/in/michael-opoku-98a1221a5/",
      image: "svgs/linkedin.svg"
    },
      {
      link : "https://github.com/NUACHE",
      image: 'svgs/github.svg'
    },
     {
      link : " https://www.fiverr.com/nuache",
      image: 'svgs/fiverr.svg'
    },
     {
      link : "https://www.upwork.com",
      image: 'svgs/upwork.svg'
    },
    ]
  }
}
}





</script>

<style>
  .bg-image {
  background-size: fill;
  height: 80px;
  width: 80px;
  border-radius: 15%;
  border: 3px solid white;
 
  margin-right: 30px;
  margin-left: 0px;
  box-shadow: none;
  -webkit-box-shadow: 0 0 5px rgb(151, 151, 151);
  -moz-box-shadow: 0 0 5px rgb(151, 151, 151);
}
</style>