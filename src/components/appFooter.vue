<template>
  <div id="hide">
  <v-bottom-navigation
    fixed
    v-model="value"
    :background-color="color"
    shift
    dark
    style="z-index: 2022"
  >
    <v-btn 
      icon
      v-for="(item, index) in bottomLists"
      :key="index"
    >
      <span>{{ item.title }}</span>
      <v-icon>{{ item.icon }}</v-icon>
    </v-btn>
  </v-bottom-navigation>
  </div>
</template>

<script>
  export default{
    data(){
      return{
        value: 0,
        bottomLists: [
          { title: 'Home', icon: 'mdi-home-outline' },
          { title: 'Categories', icon: 'mdi-format-list-bulleted' },
          { title: 'Cart', icon: 'mdi-cart-outline' },
          { title: 'Profile', icon: 'mdi-account-outline' },
        ]
      }
    },
    computed:{
      color(){
        switch(this.value){
          case 0: return 'deep-purple darken-1'
          case 1: return 'teal darken-1'
          case 2: return 'brown darken-1'
          case 3: return 'indigo darken-1'
        }
      }
    }
  };
</script>

<style>
  *{
    font-family: Lato;
  }
  @media all and (min-width: 960px){
    #hide{
      display: none;
    }
  }
</style>







<!-- <template>
  <v-footer
    color="orange"
    padless
  >
    <v-row
      justify="center"
      no-gutters
    >
      <v-btn
        v-for="link in links"
        :key="link"
        color="white"
        text
        rounded
        class="mx-2 mt-2"
      >
        {{ link }}
      </v-btn>
      <v-col
        class="orange py-2 text-center white--text"
        cols="12"
      >
        2021 xCame
      </v-col>
    </v-row>
  </v-footer>
</template>

<script>
  export default {
    data(){
    	return{
      links: [
        'Home',
        'About Us',
        'Team',
        'Services',
        'Blog',
        'Contact Us',
      ],
      }
    },
  };
</script> -->