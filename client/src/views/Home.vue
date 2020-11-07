<template>
  <div class="home">
      <v-parallax
      class="parallax"
    dark
    src="https://cdn.vuetifyjs.com/images/backgrounds/vbanner.jpg"
  >
    <v-row
      align="center"
      justify="center"
    >
      <v-col
        class="text-center"
        cols="12"
      >
        <h1 class="display-1 font-weight-thin mb-4">
          Vuetify
        </h1>
        <h4 class="subheading">
          Build your application today!
        </h4>
      </v-col>
    </v-row>
  </v-parallax>

  <v-container>
    <v-row dense>
      <v-col v-for="n in 146" :key="n">
        <v-card elevation="2">
              <v-img height="250" src="https://cdn.vuetifyjs.com/images/cards/cooking.png"></v-img>
               <v-card-title>CSGO MOD #{{n}}</v-card-title>
      <v-card-text>
        <v-rating :value="4.5" color="amber" dense half-increments readonly size="14"></v-rating> 
        <div>4.5 (413)</div>
      <div>Small plates, salads & sandwiches - an intimate setting with 12 indoor seats plus patio seating.</div>
    </v-card-text>
        <v-card-actions>
      <!-- <v-btn
        color="primary"
        depressed
      >
        <v-icon left>mdi-cart</v-icon>add to cart
      </v-btn> -->
            <v-btn
        depressed
        disabled
      >
        <v-icon left>mdi-check</v-icon>Already in cart
      </v-btn>
            <v-btn
        depressed
      >
        <v-icon left>mdi-eye</v-icon>View
      </v-btn>
    </v-card-actions>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
  
  </div>
</template>

<script>
// @ is an alias to /src

export default {
  name: "Home"
};
</script>
