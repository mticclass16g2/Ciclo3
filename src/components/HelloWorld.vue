<template>
  <v-container>
	<v-row cols="12" class="my-1">
      <v-card>
        <v-img
          src="https://i.ibb.co/rxRGLHP/reactivate-seccion-01-encabezado.jpg"
          class="white--text"
          rounded-lg 
          cover
          pa-1
        >
        <v-card-text class="text-h5 font-weight-bold mt-6">
          <v-row>
          <v-spacer></v-spacer>
              <v-btn rounded color="#364c63" dark class="mb-6" @click="verlogin"
                >Iniciar Sesión</v-btn
              >
              <v-btn
                rounded
                color="success"
                dark
                class="mb-6"
                @click="crearperfil"
                >Únete y crea tu perfil</v-btn
              >          
          </v-row>
          <v-row class="mb-10"></v-row>
            <v-row align="center" style="widt: 100%">
              <v-col cols="3"></v-col>
              <v-col class="text-h2" cols="6">
                <p></p>
                <br />
                <p style="font-size: 1.25rem; text-align: center"></p>
              </v-col>
              <v-col cols="3"></v-col>
            </v-row>
        </v-card-text>
        </v-img>        
      </v-card>
    </v-row>    
    <v-row class="text-center" style="max-width:100%;">
      <v-row class="mt-6">
        <v-col class="mb-5" cols="6">
        <v-img
        class="rounded-lg pa-4" 
        src="https://i.ibb.co/F66X0X4/reactivate-seccion-02.jpg"              
        >
        </v-img>        
          </v-col>
        <v-col class="mb-5" cols="6">
          <h2 class="font-weight-bold mb-3">
            !Registrate y ofrece tus servicios como experto profesional hoy
            mismo!
          </h2>
          
          <v-btn rounded color="#364c63" dark class="mb-6" @click="crearperfil">
            Crear mi perfil profesional
          </v-btn>

          <h2 class="font-weight-bold mb-3">
            !Encuentra aquí el profesional que estas necesitando!
          </h2>
          <v-text-field
              label="Escribe aquí tu busqueda..."
              rounded
              color="blue lighten-4"
              class="mx-auto my-0"
              dense
              outlined
          ></v-text-field>
          <v-btn rounded color="#364c63" dark class="mb-6">
          Buscar un profesional experto
          </v-btn>                 
          </v-col>
      </v-row>
      <v-row>
        <v-col class="mb-5" cols="12">
        <h2 class="display-2 font-weight-bold mb-3">
          Categorías de Expertos
        </h2>
        </v-col>
      </v-row>
    </v-row>
  </v-container>
</template>

<script>
  export default {
    name: 'HelloWorld',

    data: () => ({}),

    methods: {
    verlogin() {
      this.$router.push("login");
      // this.$router.push({name: 'login', path: '/login'})
    },
    crearperfil() {
      this.$router.push("suscripciones");
      // this.$router.push({name: 'suscripciones', path: '/suscripciones'})
    },
  },
};  
</script>

<style scoped>
.bg {
  background: url("https://i.ibb.co/hZ0QW0k/react-vate-banner-1920x1080.jpg")
  no-repeat center center;
  object-fit: cover;
  width: 100%;
 }
</style>
