
<template>
  <v-footer
    dark
    padless
  >
    <v-card
      flat
      tile
      class="red lighten-2 white--text text-center"
    >
      <v-card-text>
        <v-btn
          v-for="icon in icons"
          :key="icon"
          class="mx-4 white--text"
          icon
        >
          <v-icon size="24px">{{ icon }}</v-icon>
        </v-btn>
      </v-card-text>
      <v-card-text class="font-weight-bold">
          <h3>I believe in building strong network is essential to learning and growth and therefore, I love to connect with people from various walks of lifeand learn from their experiences and stories because 'Life is the biggest teacher in every domain of life',according to me.Let's connect!</h3>
      </v-card-text>
     
      <v-divider></v-divider>

      <v-card-text class="white--text">
        {{ new Date().getFullYear() }} — <strong>Sayani Mallick</strong>
      </v-card-text>
    </v-card>
  </v-footer>
</template>

<script>
  export default {
    data: () => ({
      icons: [
        'mdi-facebook',
        'mdi-github',
        'mdi-linkedin',
        'mdi-instagram',
      ],
    }),
  }
</script>