<template>
  <v-app>
    <v-app-bar
      app
      color="amber lighten-1"
      dark
      fixed
      elevate-on-scroll
    >
      <v-app-bar-nav-icon @click.stop="drawer = !drawer"></v-app-bar-nav-icon>
      <v-toolbar-title>xCame</v-toolbar-title>
      <v-spacer></v-spacer>

      <v-btn 
        icon
        class="mx-2"
        @click="toggleSearch"
      >
        <v-icon>mdi-magnify</v-icon>
      </v-btn>


      <v-menu offset-y>
        <template v-slot:activator="{ on, attrs }">
          <v-btn
            color="transparent"
            v-bind="attrs"
            v-on="on"
            elevation="0"
            class="mr-2 smHide"
          >
          Categories
          </v-btn>
      </template>
        
        <v-list>
          <v-list-item v-for="(item, index) in categories" :key="index" @click="onClick(item.route)">
            <v-list-item-title>{{ item.title }}</v-list-item-title>
          </v-list-item>
        </v-list>
      </v-menu>

      <v-btn 
        color="transparent" 
        elevation="0" 
        class="mr-2 smHide"
      >
        About us
      </v-btn>

      <v-btn 
        color="transparent" 
        elevation="0" 
        class="mr-2 smHide"
      >
        Contact us
      </v-btn>

      <!-- Cart icon -->
      <span class="smHide">
        <v-badge
          content="2"
          overlap
          color="orange darken-2"
          offset-x="28"
          offset-y="22"
          class="smHide"
        >
          <v-btn 
          icon
          class="mr-2 smHide"
          >
            <v-icon>mdi-cart-outline</v-icon>
          </v-btn>
        </v-badge>
        </span>


      <!-- Login icon -->
      <v-tooltip bottom>
        <template v-slot:activator="{ on, attrs }">
          <v-btn 
          icon
          class="mr-2"
          v-on="on"
          v-bind="attrs"
          >
            <v-icon>mdi-login</v-icon>
          </v-btn>          
        </template>
        <span>Login</span>
      </v-tooltip>
      
    </v-app-bar>


    <!-- Search field -->
    <v-main>
        <v-container>
          <v-expand-transition>
            <v-text-field
              v-show="isClicked"
              outlined
              dense
              label="Search"
              placeholder="More than you know..."
              clearable
            ></v-text-field>
          </v-expand-transition>
        </v-container>
      
    

    <!-- Navigation drawer -->
    <v-navigation-drawer
      v-model="drawer"
      temporary
      fixed
    >
      <v-list
        shaped
        nav
        dense
        height="400"
      >
        <v-list-item-group
          v-model="group"
          active-class="amber--text text--amber-4"
        >
          <v-list-item v-for="(item, index) in navLists" :key="index" >
            <v-list-item-icon>
              <v-icon :color="item.color">{{ item.icon }}</v-icon>
            </v-list-item-icon>
            <v-list-item-content>
              <v-list-item-title>{{ item.title }}</v-list-item-title>  
            </v-list-item-content>
          </v-list-item>


        </v-list-item-group>        
      </v-list>      
    </v-navigation-drawer>

    <single-product />
    <div style="height:1000px;"></div>

    <app-footer />
    </v-main>
  </v-app>
</template>

<script>
import appFooter from '../components/appFooter.vue'
import singleProduct from '../components/singleProduct.vue'

  export default{
    components:{
      appFooter,
      singleProduct,
    },
    data(){
      return{
        drawer: false,
        isClicked: false,
        group: null,
        navLists: [
          { title: 'Home', icon: 'mdi-home', color: 'teal' },
          { title: 'Search', icon: 'mdi-magnify', color: 'orange'  },
          { title: 'Profile', icon: 'mdi-account', color: 'deep-purple' },
          { title: 'Delete', icon: 'mdi-delete', color: 'grey'  },
          { title: 'Phone', icon: 'mdi-phone', color: 'success'  },
          { title: 'Github', icon: 'mdi-github', color: 'black'  },          
          { title: 'Gitlab', icon: 'mdi-gitlab', color: 'yellow darken-1'  },
          { title: 'Google', icon: 'mdi-google', color: 'indigo'  },
          { title: 'Facebook', icon: 'mdi-facebook', color: 'indigo'  },
          { title: 'Twitter', icon: 'mdi-twitter', color: 'indigo'  },
          { title: 'Instagram', icon: 'mdi-instagram', color: 'red lighten-1'  },
          { title: 'Linkedin', icon: 'mdi-linkedin', color: 'deep-purple'  },
          { title: 'Chat', icon: 'mdi-chat', color: 'success darken-3'  },
        ],
        categories:[
          {title: 'Clothes', route: '/jackets'},
          {title: 'Phone',  route: '/phone'},
          {title: 'Computer',  route: '/computer'},
          {title: 'T-shirt',  route: '/tshirt'},
          {title: 'Shoes', route: '/shoes'},
          {title: 'Jeans', route: 'jeans'},
          {title: 'Watches', route: '/watches'}
        ]
      }
    },
    methods:{
      toggleSearch(){
        this.isClicked = !this.isClicked; 
      },
      onClick(query){
        this.$router.push(query);
      }
    }
  };
</script>

<style>
  @media all and (max-width: 750px){
    .smHide{
      display:none;
    }
  }
</style>
