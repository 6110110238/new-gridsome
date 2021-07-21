<template>
  <v-footer dark padless class="mt-5">
    <v-card
      flat
      tile
      class="primary white--text text-center align-self-md-stretch"
      width="100%"
    >

      <v-card-text class="white--text pt-0">
        240-420 Web Eng & Apps
        | made with <v-icon class="red--text">fa-heart</v-icon> by Nuntipat Pantarag
      </v-card-text>

      <v-card-text>
        <v-btn href="https://www.facebook.com/nuntipat.get/" target="_blank" class="mx-4 white--text" icon
          ><v-icon size="24px">fab fa-facebook</v-icon></v-btn
        >
        <v-btn href="https://www.instagram.com/ggetnunti/" target="_blank" class="mx-4 white--text" icon
          ><v-icon size="24px">fab fa-instagram</v-icon></v-btn
        >
      </v-card-text>

      <v-divider></v-divider>

      <v-card-text class="white--text">
        {{ new Date().getFullYear() }} — <strong>Vuetify</strong>
      </v-card-text>
    </v-card>
  </v-footer>
</template>
