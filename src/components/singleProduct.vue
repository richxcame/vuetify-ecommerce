<template>
  <div class="mt-3">
    <v-row>
      <v-col
        cols="12"
        sm="6"
        md="4"
        class="d-flex justify-space-around"
      >
      <v-hover v-slot="{ hover }" open-delay="100" close-delay="100">
          <v-card
            :elevation="hover ? 10 : 2"
            class="mx-2 mb-2 "
            :class="{ 'on-hover' : hover }"
            color="grey lighten-4"
            style="float:left;"
          >
            <v-img
              :aspect-ratio="16/9"
              src="../assets/photo1.jpg"
            >
              <v-expand-transition>
                <div
                  v-if="hover"
                  class="d-flex transition-fast-in-fast-out orange display-1 darken-1 v-card--reveal white--text"
                  style="height: 100%;"
                >
                  $99<sup><small>.99</small></sup>
                </div>
              </v-expand-transition>
            </v-img>
            <v-card-text
              class="pt-6"
              style="position: relative;"
            >
              <v-btn
                absolute
                color="orange"
                class="white--text"
                fab
                right
                top
              >
                <v-icon>mdi-cart</v-icon>
              </v-btn>
              <h4 class="display-1 font-weight-light orange--text mb-2">
                Lorem ipsum
              </h4>
              <div class="font-weight-light mb-2">
                Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod
                tempor...
              </div>
            </v-card-text>
          </v-card>
        </v-hover>
        </v-col>
        <v-col
        cols="12"
        sm="6"
        md="4"
        class="d-flex justify-space-around"
      >
      <v-hover v-slot="{ hover }" open-delay="100" close-delay="100">
          <v-card :elevation="hover ? 10 : 2"
            class="mx-2 mb-2 "
            :class="{ 'on-hover' : hover }"
            color="grey lighten-4"
            style="float:left;"
          >
            <v-img
              :aspect-ratio="16/9"
              src="../assets/photo1.jpg"
            >
              <v-expand-transition>
                <div
                  v-if="hover"
                  class="d-flex transition-fast-in-fast-out orange display-1 darken-1 v-card--reveal white--text"
                  style="height: 100%;"
                >
                  $99<sup><small>.99</small></sup>
                </div>
              </v-expand-transition>
            </v-img>
            <v-card-text
              class="pt-6"
              style="position: relative;"
            >
              <v-btn
                absolute
                color="orange"
                class="white--text"
                fab
                right
                top
              >
                <v-icon>mdi-cart</v-icon>
              </v-btn>
              <h4 class="display-1 font-weight-light orange--text mb-2">
                Lorem ipsum
              </h4>
              <div class="font-weight-light mb-2">
                Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod
                tempor...
              </div>
            </v-card-text>
          </v-card>
        </v-hover>
        </v-col>
        <v-col
        cols="12"
        sm="6"
        md="4"
        class="d-flex justify-space-around"
      >
      <v-hover v-slot="{ hover }" open-delay="100" close-delay="100">
          <v-card :elevation="hover ? 10 : 2"
            class="mx-2 mb-2 "
            :class="{ 'on-hover' : hover }"
            color="grey lighten-4"
            style="float:left;"
          >
            <v-img
              :aspect-ratio="16/9"
              src="../assets/photo1.jpg"
            >
              <v-expand-transition>
                <div
                  v-if="hover"
                  class="d-flex transition-fast-in-fast-out orange display-1 darken-1 v-card--reveal white--text"
                  style="height: 100%;"
                >
                  $99<sup><small>.99</small></sup>
                </div>
              </v-expand-transition>
            </v-img>
            <v-card-text
              class="pt-6"
              style="position: relative;"
            >
              <v-btn
                absolute
                color="orange"
                class="white--text"
                fab
                right
                top
              >
                <v-icon>mdi-cart</v-icon>
              </v-btn>
              <h4 class="display-1 font-weight-light orange--text mb-2">
                Lorem ipsum
              </h4>
              <div class="font-weight-light mb-2">
                Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod
                tempor...
              </div>
            </v-card-text>
          </v-card>
        </v-hover>
        </v-col>
    </v-row>
  </div>
</template>

<style>
*{
  font-family: Lato;
}

.v-card--reveal {
  align-items: center;
  bottom: 0;
  justify-content: center;
  opacity: .5;
  position: absolute;
  width: 100%;
}
</style>