<template>
  <div class='wrapper'>
    <v-layout

      justify-center
      align-center
      tag='section'
      class='home'
    >
      <v-flex
        xl8
      >
    
          <h1 class='display-3 text-lg-center mb-4'>My SSR Blog!</h1>
          <p class='text-lg-center'>
            Lorem ipsum dolor sit amet, consectetur adipiscing elit, 
            sed do eiusmod tempor incididunt ut labore et dolore magna 
            aliqua. Ut enim ad minim veniam, quis nostrud exercitation 
            ullamco laboris nisi ut aliquip ex ea commodo consequat. 
            Duis aute irure dolor in reprehenderit in voluptate velit 
            esse cillum dolore eu fugiat nulla pariatur. Excepteur sint 
            occaecat cupidatat non proident, sunt in culpa qui officia 
            deserunt mollit anim id est laborum.
          </p>
      
      
      </v-flex>
    </v-layout>
    <v-layout

      justify-center
      align-center
      class='pg-PostHeader purple darken-4'
    >
      <v-flex
        xl8
      >
    
          <h2 class='display-1 text-lg-center pg-PostHeader_Title'>My latest posts:</h2>
          
      </v-flex>
    </v-layout>
    <v-layout
      justify-center
      align-center
    >
      <v-flex
        xl8
      >
        <AppGallery :posts='posts'/>
      </v-flex>
    </v-layout>
    <v-layout
      justify-center
      align-center
      tag='section'
      class='pg-Contact'
    >
      <v-flex
        xl8
      >
        <h2 class='display-1 text-lg-center'>Contact Us</h2>
        <AppContactForm/>
      </v-flex>
    </v-layout>
  </div>
</template>

<script>
import Logo from '~/components/Logo.vue'
import VuetifyLogo from '~/components/VuetifyLogo.vue'
import AppGallery from '~/components/ui/AppGallery'
import AppContactForm from '~/components/ui/AppContactForm'

export default {
  components: {
    Logo,
    VuetifyLogo,
    AppGallery,
    AppContactForm
  },
  data () {
    return {
      posts: [
        {
          id: 1,
          title: 'Post 1',
          text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.'
        },
        {
          id: 2,
          title: 'Post 2',
          text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.'
        },
        {
          id: 3,
          title: 'Post 3',
          text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.'
        },
        {
          id: 4,
          title: 'Post 3',
          text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.'
        },
        {
          id: 5,
          title: 'Post 3',
          text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.'
        }
      ]
    }
  }
}
</script>
<style lang="styl">
  section
    padding 70px 0
  .pg-Contact
    background-color #cccccc2b
  .pg-PostHeader
    min-height: 100px
    &_Title
      color #fff
</style>
