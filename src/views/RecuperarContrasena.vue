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
          Recuperar Contraseña
        </v-card-title>
        <v-card-subtitle class="justify-center">
          Ingresa aquí tu correo electrónico y recibe una contraseña temporal para acceder a tu perfil
        </v-card-subtitle>
        <v-divider class="mx-4"></v-divider>
        <v-card-text>
          <v-text-field
            label="Correo electrónico"
            prepend-icon="mdi-account-circle"
          />
        </v-card-text>

        <v-card-actions>
          <v-btn rounded color="#364c63" dark class="mb-6" @click="verlogin"
            >Reestablecer mi contraseña</v-btn
          >

        <v-divider class="mx-4"></v-divider>

        <v-card-title> Volver a iniciar sesión </v-card-title>

      </v-card>
    </v-content>
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      showPassword: false,
    };
  },
};
</script>
