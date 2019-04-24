<template>
 
  <v-card nuxt>
    <nuxt-link :to="/blog/+info.id">
      <v-img
        class="white--text"
        height="200px"
        src="https://cdn.vuetifyjs.com/images/cards/docks.jpg"
      >
    
        <v-container fill-height fluid>
          <v-layout fill-height>
            <v-flex xs12 align-end flexbox>
              <span class="headline">Top 10 Australian beaches</span>
            </v-flex>
          </v-layout>
        </v-container>
      </v-img>
    </nuxt-link>
    <v-card-title>
      <div>
        <span class="grey--text">Number 10</span><br>
        <span>Whitehaven Beach</span><br>
        <span>Whitsunday Island, Whitsunday Islands</span>
      </div>
    </v-card-title>
    <v-card-text>
      <p>
        {{info.text}}
      </p>
    </v-card-text>
    <v-card-actions>
      <v-btn flat color="orange">Share</v-btn>
      <v-btn flat color="orange" nuxt :href='/blog/+info.id'>Explore</v-btn>
    </v-card-actions>
  </v-card>
</template>
<script>
export default {
  name: 'AppPostCard',
  props: {
    info: {
      type: Object
    }
  }
}
</script>
<style lang="styl" scoped>
  a
    text-decoration none
</style>