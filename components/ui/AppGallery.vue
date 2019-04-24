<template>
  <div class='pg-Gallery'>
    <v-container fill-height fluid>
      <v-layout tag='ul'row wrap class='pg-Gallery_list'>
        <v-flex tag='li' class='pa-4' v-for='post in posts' :key='post.id' xl4>
          <AppPostCard   :info='post'  />
        </v-flex>
      </v-layout>
    </v-container> 
  </div>
</template>
<script>
import AppPostCard from './AppPostCard'
export default {
  props: ['posts'],
  components: {
    AppPostCard
  }
}

</script>
<styles lang='styl'>

  ul
    padding 0
  li
    list-style: none
</styles>