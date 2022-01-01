<template>
  <MDBRow style="padding-left: 25px; padding-right: 25px">
    <MDBCol col="3">Projects</MDBCol>
    <MDBCol col="9" style="display: flex; flex-wrap: wrap;" >
     <div class="bg-image"  v-bind:style="{ 'background-image': 'url(' +'svgs/linkedin.svg'  + ')' }">
         
          </div>
      <div class="bg-image"  v-bind:style="{ 'background-image': 'url(' +'svgs/github.svg'  + ')' }">
         
          </div>
          <div class="bg-image"  v-bind:style="{ 'background-image': 'url(' +'svgs/fiverr.svg'  + ')' }">
         
          </div>
           <div class="bg-image"  v-bind:style="{ 'background-image': 'url(' +'svgs/upwork.svg'  + ')' }">
         
          </div>
         
    </MDBCol>
  
  
  </MDBRow>
</template>

<script>
import {  MDBCol, MDBRow } from "mdb-vue-ui-kit";

export default {
   components: {
  MDBCol, MDBRow, 
  },
  
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