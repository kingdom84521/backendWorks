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
  </v-app>
</template>

<script>
import header from '@/components/common/Header.vue'

export default {
  name: 'App',
  components: {
    Header: header
  },

  data: () => ({
    //
  }),
};
</script>

<style scoped>
</style>
