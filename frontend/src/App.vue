<template>
  <v-app>
    <v-row no-gutters justify="center">
      <v-col cols="10">
        <v-sheet color="#F3F3F3">
          <Header></Header>
          <router-view />
        </v-sheet>
      </v-col>
    </v-row>
    <User-Menu></User-Menu>
  </v-app>
</template>

<script>
import header from '@/components/common/Header.vue'
import userMenu from '@/components/common/UserMenu.vue'

export default {
  name: 'App',
  components: {
    Header: header,
    UserMenu: userMenu,
  },

  data: () => ({
    //
  }),
};
</script>

<style scoped>
  .user-menu {
    width: 40px ;
    height: 75px ;
    border-radius: 0px 76px 76px 0px ;
    background-color: crimson;
    position: fixed;
    left: 8.4%;
    bottom: 50%;
  }
</style>
