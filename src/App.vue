<template>
  <v-app>
    <v-toolbar color="#364c63" dense max-height="50">
  <v-app-bar-nav-icon to="/"></v-app-bar-nav-icon>
  <v-toolbar-title class="white--text">Inicio</v-toolbar-title>
  <v-spacer></v-spacer>
  <v-toolbar-items>
        <v-btn color="white" text rounded class="my-auto" to="nosotros"
          >Nosotros</v-btn
        >
        <v-btn color="white" text rounded class="my-auto" to="noticias"
          >Noticias</v-btn
        >
        <v-btn color="white" text rounded class="my-auto" to="suscripciones"
          >Suscripciones</v-btn
        >
        <v-btn color="white" text rounded class="my-auto" to="servicios"
          >Servicios</v-btn
        >
        <v-btn color="white" text rounded class="my-auto" to="login"
          >Iniciar Sesión</v-btn
        >
  </v-toolbar-items>
  </v-toolbar>

    <v-main>
      <router-view />
    </v-main>

    <v-footer color="#364c63" class="mt-10" padless>
      <v-row justify="center" no-gutters>
      <v-btn
          v-for="(link, icon) in icons"
          :key="icon"
          class="mx-4 white--text"
          icon
          :href="link"
          target="_blank"
        >
          <v-icon size="24px">
            {{ icon }}
          </v-icon>
        </v-btn>      
        <v-btn
          v-for="(link, key) in links"
          :key="link"
          color="white"
          text
          rounded
          class="my-2"
          :to="link"
        >
          {{ key }}
        </v-btn>
        <v-col class="primary lighten-2 py-4 text-center white--text" cols="12">
          <strong>
            (c) {{ new Date().getFullYear() }} Reactívate -
            <a
              href="https://github.com/mticclass16g2"
              title="Repositorio GitHub - Grupo 16 Equipo 2"
              target="_blank"
            >
              Grupo 16 Equipo Desarrollo de Software No. 2
            </a>
            | MISIÓN TIC 2022
          </strong> 
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
      Suscripciones: 'suscripciones',
      Servicios: 'servicios',
      Blog: 'blog',
      Contáctenos: 'contactenos',
      },
       icons: {
      "mdi-whatsapp":
        "https://api.whatsapp.com/send?phone=+579999999999&text=%C2%A1Bienvenido%20a%20React%C3%ADvate!%20%C2%BFCu%C3%A9ntanos%20como%20podemos%20ayudarte?",
      "mdi-mail": "mailto:re-activateco@outlook.com",
      "mdi-linkedin": "https://www.linkedin.com/company/re-activateco",
      "mdi-instagram": "https://www.instagram.com/re_activateco/",
       },     
  }),
};
</script>

<style scoped>

</style>
