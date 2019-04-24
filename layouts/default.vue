<template>
  <v-app complex>
   
    <v-toolbar
      :clipped-left="clipped"
      fixed
      app
    >
    
          <v-toolbar-items>
            <v-btn flat v-for="item in links" :key="item.link" :to='item.link' nuxt>
              {{item.title}}
            </v-btn>
          </v-toolbar-items>
  
    </v-toolbar>
    <v-content>
      <v-container fluid class='pa-0'>
        <nuxt />
      </v-container>
    </v-content>
    <v-navigation-drawer
      v-model="rightDrawer"
      :right="right"
      temporary
      fixed
    >
      <v-list>
        <v-list-tile @click.native="right = !right">
          <v-list-tile-action>
            <v-icon light>compare_arrows</v-icon>
          </v-list-tile-action>
          <v-list-tile-title>Switch drawer (click me)</v-list-tile-title>
        </v-list-tile>
      </v-list>
    </v-navigation-drawer>
    <v-footer
      :fixed="fixed"
      app
    >
      <span>&copy; 2019</span>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      active:'test',
      clipped: false,
      drawer: false,
      fixed: false,
      links: [
        {
          title: 'Home',
          link: '/'
        },
        {
          title: 'About',
          link: '/about'
        }
        ],
      items: [
        {
          icon: 'apps',
          title: 'Welcome',
          to: '/'
        },
        {
          icon: 'bubble_chart',
          title: 'Inspire',
          to: '/inspire'
        }
      ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: 'Vuetify.js'
    }
  }
}
</script>
