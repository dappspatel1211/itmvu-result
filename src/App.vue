<template>
  <v-app>
    
    <v-toolbar
      app
      :clipped-left="clipped"

  color="pink darken-4"
    >
    
      
     
        <v-toolbar-title class="white--text">Profile</v-toolbar-title>
      <v-spacer></v-spacer>
      
    </v-toolbar>
    <v-content>
      <router-view/>
    </v-content>
    <v-card height="200px">
    <v-bottom-nav
      absolute
      shift
      :value="true"
      :active.sync="e2"
      :color="color"
    >
      <v-btn dark>
        <span>Profile</span>
        <v-icon>account_circle</v-icon>
      </v-btn>
      <v-btn dark>
        <span>Declared Results</span>
        <v-icon>assignment</v-icon>
      </v-btn>
      <v-btn dark>
        <span>External</span>
        <v-icon>done_all</v-icon>
      </v-btn>
      <v-btn dark>
        <span>Internal</span>
        <v-icon>done</v-icon>
      </v-btn>
    </v-bottom-nav>
  </v-card>
    <v-footer :fixed="fixed" app>
      <span>&copy; 2018 © ITM VOCATIONAL UNIVERSITY</span>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  data () {
    return {
      clipped: false,
      drawer: true,
      fixed: false,
      items: [{
        icon: 'bubble_chart',
        title: 'Inspire'
      }],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: 'Vuetify.js'
    }
  },
  name: 'App'
}


</script>

<script>
  export default {
    data () {
      return {
        e2: 3
      }
    },

    computed: {
      color () {
        switch (this.e2) {
          case 0: return 'pink darken-4'
          case 1: return 'pink darken-4'
          case 2: return 'pink darken-4'
          case 3: return 'pink darken-4'
        }
      }
    }
  }
</script>