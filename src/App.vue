<template>
  <v-app>
  <v-toolbar
    color="blue"
    dense
    max-height="48"
  >
  <v-app-bar-nav-icon to="/"></v-app-bar-nav-icon>
  <v-toolbar-title>Reactívate</v-toolbar-title>
  <v-spacer></v-spacer>
  <v-text-field
            label="Buscar Servicios"
  ></v-text-field>
  <v-toolbar-items>
    <v-btn icon>
      <v-icon>mdi-magnify</v-icon>
    </v-btn>
    <v-btn color="white" text rounded class="my-auto" to="nosotros">Nosotros</v-btn>
    <v-btn color="white" text rounded class="my-auto" to="noticias">Noticias</v-btn>
    <v-btn color="white" text rounded class="my-auto" to="suscripciones">Suscríbete</v-btn>
    <v-btn color="white" text rounded class="my-auto" to="servicios">Servicios</v-btn>
    <v-btn color="white" text rounded class="my-auto" to="login">Login</v-btn>
  </v-toolbar-items>
  </v-toolbar>
    <v-main>
      <router-view/>
    </v-main>
    <v-footer
      color="primary lighten-1"
      padless
      fixed
    >
      <v-row
        justify="center"
        no-gutters
      >
      <v-btn
          v-for="(link,icon) in icons"
          :key="icon"
          class="mx-4 white--text"
          icon
          :href=link
          target="blank"
        >
          <v-icon size="24px">
            {{ icon }}
          </v-icon>
        </v-btn>      
        <v-btn
          v-for="(link,key) in links"
          :key="link"
          color="white"
          text
          rounded
          class="my-2"
          :to=link
        >
          {{ key }}
        </v-btn>
        <v-col
          class="primary lighten-2 py-4 text-center white--text"
          cols="12"
        >
        <strong>Reactívate</strong> - {{ new Date().getFullYear() }} 
        </v-col>
      </v-row>
    </v-footer>    
  </v-app>
</template>

<script>

export default {
  name: 'App',

  data: () => ({
    //
      links: {
        'Suscripciones':'suscripciones',
        'Servicios':'servicios',
        'Blog':'blog',
        'Contáctenos':'contactenos',
      },
       icons: {
        'mdi-facebook': 'https://www.facebook.com/',
        'mdi-twitter':'https://twitter.com',
        'mdi-linkedin':'https://www.linkedin.com/company/re-activateco',
        'mdi-instagram':'https://www.instagram.com/?hl=es',
       },     
  }),
};
</script>
<style scoped>

</style>
