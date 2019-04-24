<template>
  <v-container>
    <v-layout tag='section' justify-center>
      <v-flex xl8>
        <h1 class='display-3 text-lg-center mb-5'>{{post.title}}</h1>
        <hr class='ma-5'>
        <p>
          {{post.text}}
        </p>
      </v-flex>
    </v-layout>
  </v-container>
</template>
<script>
export default {
  data () {
    return {
      post: {
        title: 'Тестовый пост',
        text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.'
      }
    }
  }
}
</script>