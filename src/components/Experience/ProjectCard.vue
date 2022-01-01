<template>
  <MDBCard
    style="
      box-shadow: none;
      -webkit-box-shadow: 0 0 5px rgb(151, 151, 151);
      -moz-box-shadow: 0 0 5px rgb(151, 151, 151);
    "
  >
    <MDBCardBody>
      <div>
        <div style="display: flex; flex-wrap: wrap">
          <div class="bg-image"  v-bind:style="{ 'background-image': 'url(' +'img/' + image + ')' }">
         
          </div>
          <div
            style="projectName: relative; margin-top: 10px; text-align: justify"
          >
            <div>{{ projectName }}</div>
            <div style="font-size: 15px; font-weight: 100; width: 250px  ">{{ description }}</div>
          </div>
        </div>
      </div>

     
    </MDBCardBody>
    <MDBCardFooter class="text-muted">
      <div
        class="justify-content-between"
        style="display: flex; flex-wrap: wrap"
      >
        <div>
         <slot></slot>
        </div>
        <div>
        <MDBBtn style="padding: 0px" @click="open" color="link">View Project</MDBBtn>
        </div>
      </div>
    </MDBCardFooter>
  </MDBCard>
</template>
<script>
import {
  MDBCard,
 MDBBtn,
  MDBCardBody,

  MDBCardFooter,
} from "mdb-vue-ui-kit";
export default {
  components: {
    MDBCard,
    MDBCardBody,
 MDBBtn,
   

    MDBCardFooter,
  },
  data() {
    return {
    
    };
  },
  methods :{
    open(){
     
      this.$emit('openModal')
    }
  },

  props : ['projectName', 'description', 'timeLine', 'image' ]
};
</script>

<style scoped>
.bg-image {
  background-size: fill;
  height: 80px;
  width: 80px;
  border-radius: 50%;
  border: 3px solid white;

  margin-right: 10px;
  margin-left: 0px;
  box-shadow: none;
  -webkit-box-shadow: 0 0 5px rgb(151, 151, 151);
  -moz-box-shadow: 0 0 5px rgb(151, 151, 151);
}
a {
  color: #7055a0;
  padding-right: 0px;
  padding-left: 0px;
}
</style>