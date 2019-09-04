<template>
  <v-app>
    <v-toolbar app>
      <v-toolbar-title class="headline text-uppercase">
        <span>FEED DATA FROM API</span>
      </v-toolbar-title>
    <v-divider
      class="mx-3"
      inset
      vertical
    ></v-divider>

    <span class="subheading">My Home</span>

    <v-spacer></v-spacer>

    <v-toolbar-items class="hidden-sm-and-down">
      <v-text-field
        hide-details
        prepend-icon="search"
        single-line
      ></v-text-field>    
      
      <v-btn flat>
        News
      </v-btn>

      <v-divider vertical></v-divider>

      <v-btn flat>
        Blog
      </v-btn>

      <v-divider vertical></v-divider>

      <v-btn flat>
        Music
      </v-btn>

    </v-toolbar-items>
    </v-toolbar>
    <v-content>
      <v-btn color="success">Success</v-btn>
    </v-content>
  </v-app>
</template>

<script>
import axios from "axios";
export default {
  name: 'App',
  components: {

},
  data () {
    return {
      //
    }
  },
  created() {
    axios.get('http://10.0.10.88:8000/hotel')
    .then((res)=>{
      console.log(res.data)
    })
    .catch(err => console.log(err))
  },
}
</script>
