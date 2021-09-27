<template>
  <v-container>
	<v-row cols="12" class="my-1">
      <v-card>
        <v-img
          :src="require('../assets/reactivate-seccion-01-encabezado-sin-texto.jpg')"
          class="white--text"
          rounded-lg 
          cover
          pa-1
        >
        <v-card-text class="text-h5 font-weight-bold mt-6">
          <v-row>
          <v-spacer></v-spacer>
          <v-btn
            rounded
            color="primary"
            dark
            class="mb-6"
          >Inicar Sesión</v-btn>
          <v-btn
            rounded
            color="primary"
            dark
            class="mb-6 mx-3"
          >Unete y crea tu perfil</v-btn>          
          </v-row>
          <v-row class="mb-10"></v-row>
          <v-row align="center" style="widt:100%;">
            <v-col cols="3"></v-col>
            <v-col
                class="text-h3"
                cols="6"
              >
              <p>Reactívate Colombia</p>
              <p style="font-size:1.25rem;text-align:center;">El directorio de profesionales y empresas para la reactivación ecónomica en Colombia</p>
            </v-col>
            <v-col cols="3"></v-col>
          </v-row>
        </v-card-text>
        </v-img>        
      </v-card>
    </v-row>    
    <v-row class="text-center" style="max-width:100%;">
      <v-row class="mt-6">
          <v-col
        class="mb-5"
        cols="6"
        >
        <v-img
        class="rounded-lg pa-4" 
        src="https://i.ibb.co/F66X0X4/reactivate-seccion-02.jpg"              
        >
        </v-img>        
          </v-col>
          <v-col
            class="mb-5"
            cols="6"        
          >
          <h2 class="font-weight-bold mb-3">
            !Registrate y ofrece tus servicios como experto profesional hoy mismo!
          </h2>
          <v-btn
            rounded
            color="primary"
            dark
            class="mb-6"
          >Crear mi perfil profesional</v-btn>
          <h2 class=" font-weight-bold mb-3">
            !Encuentra aquí el profesional que estas necesitando!
          </h2>
          <v-text-field
              label="escribe tus busquedas"
              rounded
              color="blue lighten-4"
              class="mx-auto my-0"
              dense
              outlined
          ></v-text-field>
          <v-btn
            rounded
            color="primary"
            dark
          >
          Buscar un profesional experto
          </v-btn>                 
          </v-col>
      </v-row>
      <v-row>
        <v-col 
        class="mb-4"
        cols="12"
        >
        <p class="subheading font-weight-regular">
          <br>
          <a
            href="https://drive.google.com/drive/folders/1PyujRrTVDCl_JHfyghcif5svhz3y42YE"
            target="_blank"
          > Somos el grupo 16 equipo de desarrollo No 2</a>
        </p>
        </v-col>
        <v-col
        class="mb-5"
        cols="12"
      >
        <h2 class="display-2 font-weight-bold mb-3">
          Categorias de Expertos
        </h2>
        </v-col>
      </v-row>
    </v-row>
  </v-container>
</template>

<script>
  export default {
    name: 'HelloWorld',

    data: () => ({


    }),
  }
</script>
<style scoped>
.bg {
  background: url("../assets/reactivate-seccion-01-encabezado-sin-texto.jpg") no-repeat center center;
  object-fit: cover;
  width: 100%;
 }
</style>
