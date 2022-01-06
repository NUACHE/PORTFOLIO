<template>
  <MDBCard
    style="
      box-shadow: none;
      -webkit-box-shadow: 0 0 5px rgb(151, 151, 151);
      -moz-box-shadow: 0 0 5px rgb(151, 151, 151);
      margin-top:15px;
    "
  >
    <MDBCardBody>
      <div>
        <div style="display: flex; flex-wrap: wrap">
          <div class="bg-image"  v-bind:style="{ 'background-image': 'url(' +'img/' + image + ')' }">
         
          </div>
          <div
            style="position: relative; margin-top: 20px; text-align: justify"
          >
            <div>{{ position }}</div>
            <div style="font-size: 15px; font-weight: 100">{{ company }}</div>
          </div>
        </div>
      </div>

      <MDBCardText
        style="
          text-align: left;
          font-size: 15px;
          font-weight: 100;
          padding-top: 10px;
          padding-left: 0px;
          display: flex;
          flex-wrap: wrap;
        "
      >
       {{timeLine}}
      </MDBCardText>
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
        <MDBBtn style="padding: 0px" @click="open" color="link">View Projects</MDBBtn>
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
  MDBCardText,
  MDBCardFooter,
} from "mdb-vue-ui-kit";
export default {
  components: {
    MDBCard,
    MDBCardBody,
 MDBBtn,
    MDBCardText,

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

  props : ['position', 'company', 'timeLine', 'image' ]
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