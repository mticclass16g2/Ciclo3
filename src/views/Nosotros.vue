<template>
  <v-content>
    <v-container>
      <div>
        <h1>NOSOTROS</h1>
        <br />
        <v-img
          contain
          height="500"
          src="https://i.ibb.co/BG5dfkH/profesiones-03-1920x1080.png"
        ></v-img>
        <br />
        <h2>Somos Reactívate</h2>
        <br />
        <p>
          El directorio más completo y gratuito de profesionales y empresas para
          la reactivación económica en Colombia.
          <br />
          <br />
          Si eres profesional, empresario, dueño de negocio o tienes un producto
          o servicio para ofrecer; te invitamos a registrarte de forma gratuita
          en nuestro portal; así tendrás la posibilidad de dar a conocer tu
          actividad económica; teniendo una mayor posibilidad de encontrar ese
          cliente que te ayudará a generar ingresos para ti y tu familia.
        </p>
        <br />
        <v-divider></v-divider>
        <br />
        <h2>¿Quiénes Somos?</h2>
        <br />
        <p>
          Nuestra organización está conformada por un equipo de cuatro
          profesionales en diferentes áreas, que a través de esta solución
          buscan que todos los colombianos, unidos, logremos salir adelante en
          esta nueva realidad que la pospandemia nos ha planteado.
        </p>
        <br />
      </div>
      <v-row dense>
        <v-col>
          <v-card hover class="mx-auto">
            <v-card-actions class="justify-center">
              <v-img
                contain
                width="250"
                src="https://i.ibb.co/94GfQqM/julio-cortes-trujillo-perfil-500x500.png"
              ></v-img>
            </v-card-actions>
            <v-card-title class="justify-center">
              <h3>Julio<br>
              Cortés Trujillo</h3>
              </h3>
            </v-card-title>
            <v-divider class="mx-4"></v-divider>
            <v-card-subtitle style="text-align: center"
              >Ingeniero Electricista
              <br />
              Universidad Nacional de Colombia</v-card-subtitle
            >
            <v-card-text>
              Consultor en software libre, docente universitario en
              Investigación y miembro activo de grupo VIRTUS que trabaja en
              Ambientes Virtuales de Aprendizaje.
              <br />
              <br />
              Coautor de los libros “Dificultades de la escritura en la
              Educación Superior” (2008) y “Realidad virtual en los procesos de
              enseñanza en la Educación Superior” (2019).
              <br />
              <br />
              Sus aficiones principales son el tenis de campo, senderismo por
              Colombia, la lectura y escritura sobre tecnología.
            </v-card-text>
          </v-card>
        </v-col>
        <v-col>
          <v-card hover class="mx-auto">
            <v-card-actions class="justify-center">
              <v-img
                contain
                width="250"
                src="https://i.ibb.co/dMxjFWv/carlos-eduardo-sanchez-guevara-perfil-500x500.png"
              ></v-img>
            </v-card-actions>
            <v-card-title class="justify-center">
              <h3>Carlos Eduardo</h3>
              <h3>Sánchez Guevara</h3>
            </v-card-title>
            <v-divider class="mx-4"></v-divider>
            <v-card-subtitle style="text-align: center"
              >Administrador de Empresas
              <br />
              Pontificia Universidad Javeriana - Cali</v-card-subtitle
            >
            <v-card-text>
              Cuenta con una experiencia de más de 15 años en el área comercial,
              mercadeo empresarial y marketing digital en compañías de
              tecnología.
              <br />
              <br />
              Experto en el diseño de sitios web, tiendas online y desarrollo de
              aplicaciones.
              <br />
              <br />
              Sus aficiones principales son la música, la natación, la lectura y
              disfrutar junto a su familia de actividades al aire libre.
            </v-card-text>
          </v-card>
        </v-col>
        <v-col>
          <v-card hover class="mx-auto">
            <v-card-actions class="justify-center">
              <v-img
                contain
                width="250"
                src="https://i.ibb.co/YN136Mx/luis-felipe-norena-lopez-perfil-500x500.png"
              ></v-img>
            </v-card-actions>
            <v-card-title class="justify-center">
              <h3>Luís Felipe</h3>
              <h3>Noreña López</h3>
            </v-card-title>
            <v-divider class="mx-4"></v-divider>
            <v-card-subtitle style="text-align: center"
              >Licenciado en Física
              <br />
              Universidad Pedagógica Nacional</v-card-subtitle
            >
            <v-card-text>
              Experiencia en Desarrollo de Aplicaciones Web, Bases de Datos,
              Frontend con Vue.js, Backend con Django. Certificación Microsoft
              en .NET Framework, Azure Repos (basado en GIT).
              <br />
              <br />
              Sus aficiones principales son la Física, la familia, el
              aprendizaje y la posibilidad de innovar.
            </v-card-text>
          </v-card>
        </v-col>
        <v-col>
          <v-card hover class="mx-auto">
            <v-card-actions class="justify-center">
              <v-img
                contain
                width="250"
                src="https://i.ibb.co/mScr1j6/cristhian-andres-morales-gomez-perfil-500x500.png"
              ></v-img>
            </v-card-actions>
            <v-card-title class="justify-center">
              <h3>Cristhian Andrés</h3>
              <h3>Morales Gómez</h3>
            </v-card-title>
            <v-divider class="mx-4"></v-divider>
            <v-card-subtitle style="text-align: center"
              >Ingeniero de Telecomunicaciones
              <br />
            </v-card-subtitle>
            <v-card-text>
              Profesional con experiencia en administración de redes de
              telecomunicaciones, con más de tres años de experiencia brindando
              soluciones de Voz sobre IP.
              <br />
              <br />
              Sus aficiones principales son los deportes individuales y el
              aprendizaje constante de nuevas tecnologías.
            </v-card-text>
          </v-card>
        </v-col>
      </v-row>

      <v-row>
        <v-col align="center">
          <div>
            <v-divider></v-divider>
            <br />
            <div><h4>Ahora que nos conoces…</h4></div>
            <br />
          </div>
          <v-btn
            rounded
            color="success"
            dark
            class="mb-6"
            @click="verlogin"
          >Únete y crea tu perfil</v-btn>
          <v-btn
            rounded
            color=#364c63
            dark
            class="mb-6"
            @click="verlogin"
          >Iniciar Sesión</v-btn>
        </v-col>
      </v-row>
    </v-container>
  </v-content>
</template>

<script>
export default {
  name: "Nosotros",

  data: () => ({}),

  methods: {
    verlogin() {
      this.$router.push("login");
      // this.$router.push({name: 'login', path: '/login'})
    },
  },
};
</script>

<style scoped>
h1 {
  text-align: center;
  color: #364c63;
}

h3 {
  text-align: center;
  color: #f3b340;
}
</style>