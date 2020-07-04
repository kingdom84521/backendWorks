<template>
  <v-col 
    class="text-center"
    cols="4"
    align-self="center"
    >
    <v-row 
      no-gutters
      class="ma-2 bg--white round-corner border"
      >
      <v-col>
        <v-row no-gutters>
          <v-col>
            <div class="ma-3 round-corner border" style="padding-bottom: 50%" v-slot:name>
            </div>
            <div class="text-start ml-3 title text-weight-black">
              {{ this.name }}
            </div>
            <div class="text-start ml-3 subtitle-1 grey--text">
              {{ this.author }}
            </div>
          </v-col>
        </v-row>
        <v-row>
          <v-col class="text-end mr-3 mb-2">
            <span class="px-6 py-3 full-rounded white--text text-weight-black title"
                  :style="`background-color: ${ this.statusValues.color }`"
                  >
              {{ this.statusValues.value }}
            </span>
          </v-col>
        </v-row>
      </v-col>
    </v-row>
  </v-col>
</template>

<script>
export default {
  props: {
    status: {
      type: String,
      default: "available"
    },
    name: {
      type: String,
      default: "我是書名我是書名我是書名"
    },
    author: {
      type: String,
      default: "我是作者"
    }
  },
  computed: {
    statusValues() {
      switch ( this.status ) {
        case "borrowed": 
          return {
            color: "#FF8080",
            value: "借出" 
          } ;
        case "newBook":
          return {
            color: "#93EF66",
            value: "新書" 
          } ;
        case "available":
          return {
            color: "#80A2FF",
            value: "在館" 
          } ;
        default:
          return 0
      }
    }
  }
}
</script>

<style>
  .bg--white {
    background-color: white;
  }
  .round-corner {
    border-radius: 5px;
  }
  .full-rounded {
    border-radius: 30px;
  }
  .border {
    border: #707070 1px solid;
  }
</style>