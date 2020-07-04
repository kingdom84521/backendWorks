<template>
  <div style="position: fixed; left: 8.4%; top: 40%; height: 32%;" class="d-flex flex-row align-center">
    <div 
      class="d-flex justify-center align-center side-menu text-center flex-column"
      @click="clickHandler"
      >
      <v-icon color="white" large>mdi-chevron-right</v-icon>
    </div>
    <div
      class="justify-center align-center window text-center flex-column"
      v-show="this.state"
      >
      <v-row no-gutters>
        <v-col>
          <div class="ma-2 image-container">
            <img src="@/assets/picture_missing.png" width="100%" height="100%">
          </div>
          <span>
            myname
          </span>
          <v-divider class="mt-2 mx-2"></v-divider>
        </v-col>
      </v-row>
    </div>
  </div>
</template>

<script>
export default {
  data: () => ({
    state: true
  }),
  methods: {
    clickHandler() {
      console.log("clicked")
      this.state = !this.state;
    }
  }
}
</script>
  
<style>
  .side-menu {
    width: 40px ;
    height: 75px ;
    border-radius: 0px 76px 76px 0px ;
    background-color: #707070;
    margin-right: 5%
    /* position: fixed; */
    /* margin-top: 75%; */
  }
  .window {
    height: 70%;
    background-color: white;
    transition: 0.3s;
    /* margin-left: 80px; */
    /* position: fixed; */
    border: #707070 1px solid;
    border-radius: 5px;
  }
  .image-container {
    max-width: 300px;
    max-height: 300px;
    background-color: violet;
    border: #707070 1px solid;
  }
</style>