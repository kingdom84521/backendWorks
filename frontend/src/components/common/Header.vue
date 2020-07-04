<template>
  <v-app-bar 
    color="transparent"
    height="277"
    elevation="0"
    >
    <v-row no-gutters class="denseUnderline" justify="space-between">
      <v-col align-self="center" cols="4">
        <v-row class="text-center">
          <v-col>
            <div 
              class="strokeText"
              style="font-size: 80px;"
              >
              圖書館系統
            </div>
          </v-col>
        </v-row>
      </v-col>
      <v-col cols="6">
        <v-row justify="end">
          <v-sheet class="mr-6 mt-4" color="transparent">
            <span class="mx-2 text-h5 clickable">
              說明中心
            </span>
            <v-divider vertical />
            <span class="mx-2 text-h5 clickable">
              註冊
            </span>
            <v-divider vertical />
            <span class="mx-2 text-h5 clickable">
              登入
            </span>
          </v-sheet>
        </v-row>
      </v-col>
    </v-row>
  </v-app-bar>
</template>

<script>
export default {

}
</script>

<style>
  .notoSansTcFamily {
    font-family: "Noto Sans TC" sans-serif;
  }
  .denseUnderline {
    height: 103% ;
    width: 100% ;
    background-color: transparent;
    border-bottom: #707070 0.5px solid;
  }
  .strokeText {
    color: #707070;
    text-shadow: 
      -1.5px -1.5px 0 #FFFFFF,  
      1.5px -1.5px 0 #FFFFFF,
      -1.5px 1.5px 0 #FFFFFF,
      1.5px 1.5px 0 #FFFFFF;
  }
  .clickable {
    cursor: pointer;
    transition: 0.25s;
  }
  .clickable:hover {
    color: #34baeb
  }
</style>