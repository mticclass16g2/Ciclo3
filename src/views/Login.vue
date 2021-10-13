<template>
  <v-app>
    <v-content>
      <v-card width="550" class="mx-auto mt-9">
        <v-img
          contain
          max-height="80"
          src="https://i.ibb.co/x15GLkz/react-vate-logo-transp-929x172.png"
        ></v-img>
        <v-card-title class="justify-center">
          Ingresa a tu cuenta
        </v-card-title>
        <v-card-text>
          <v-text-field
             v-model="this.usuario.email"
            label="Correo electrónico"
            prepend-icon="mdi-account-circle"
          />
          <v-text-field
           v-model="this.usuario.loginPassword"
            label="Contraseña"
            :type="showPassword ? 'text' : 'password'"
             prepend-icon="mdi-lock"
            :append-icon="showPassword ? 'mdi-eye' : 'mdi-eye-off'"
            @click:append="showPassword = !showPassword"
          />
        </v-card-text>

        <v-card-actions>
          <v-btn rounded color="#364c63" dark class="mb-6" @click="login"
            >Iniciar Sesión</v-btn
          >
        </v-card-actions>
        <v-alert
        dense
        border="left"
        type="warning"
        v-if="badLogin"
      >
        Usuario o contraseña incorrecto
      </v-alert>
        <v-card-text>
          <div>Olvidé mi usuario o contraseña</div>
        </v-card-text>

        <v-divider class="mx-4"></v-divider>

        <v-card-title> ¿No tienes una cuenta? Registrate ahora </v-card-title>

        <v-card-actions>
          <v-btn rounded color="success" dark class="mb-6" @click="crearperfil"
            >Registrarme</v-btn
          >
        </v-card-actions>
      </v-card>
    </v-content>
  </v-app>
</template>

<script>
export default {

  respuesta:{},
  data() {

      return {
/*       usuario:{
        email:"mman.morales@gmail.com",
        loginPassword: "1234567890",
      }, */
      usuario:{},
      showPassword: false,
      badLogin: false,
    };


  },
  methods: {
    crearperfil() {
      this.$router.push("suscripciones");
      // this.$router.push({name: 'suscripciones', path: '/suscripciones'})
    },
    async login(){

    const requestOptions = {
    method: "POST",
    headers: { "Content-Type": "application/json" },
    body: JSON.stringify(this.usuario)
    };
    await fetch ("https://reactivate-backend.herokuapp.com/logging", requestOptions)
      .then(response => response.json())
      .then(data => {
          this.respuesta = data;
          console.log('este es data:',this.respuesta);
          if (this.respuesta.message=='Longging correcto.'){
              this.$router.push('servicios')
          } else{this.badLogin=true}
           });

    }
  },
};
</script>
