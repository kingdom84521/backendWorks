<template>
  <v-container>
    <v-row class="mx-1" justify="center">
      <v-col cols="11">
        <v-row no-gutters>
          <Book v-for="index in 12" :key="`book-${index}`" status="newBook">
            <img src="@/assets/cat.jpg" v-slot:image />
          </Book>
        </v-row>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import book from '@/components/unique/Home/book.vue'

export default {
  components: {
    Book: book
  },
  data: () => ({

  })
}
</script>

<style>

</style>