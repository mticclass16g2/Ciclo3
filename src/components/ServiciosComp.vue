<template>
  <v-container>
  <v-row class="text-center">
    <v-col
    v-for=" item in servicios"
    :key="item.nombre"    
    cols="12"
    md="3"
  >
  <v-card

    class="mx-auto rounded-xl pa-1"
    max-width="344"
  >
    <v-img
      :src="item.photoUrl"
      height="200px"
      class="rounded-xl pa-1"
    
    ></v-img>

    <v-card-title>
      {{ item.nombre }}
    </v-card-title>

    <v-card-actions>
      <v-btn
        color="orange lighten-2"
        text
      >
        Explorar
      </v-btn>

      <v-spacer></v-spacer>

      <v-btn
        icon
        @click="show = !show"
      >
        <v-icon>{{ show ? 'mdi-chevron-up' : 'mdi-chevron-down' }}</v-icon>
      </v-btn>
    </v-card-actions>

    <v-expand-transition>
      <div v-show="show">
        <v-divider></v-divider>

        <v-card-text>
          I'm a thing. But, like most politicians, he promised more than he could deliver. You won't have time for sleeping, soldier, not with all the bed making you'll be doing. Then we'll go with that data file! Hey, you add a one and two zeros to that or we walk! You're going to do his laundry? I've got to find a way to escape.
        </v-card-text>
      </div>
    </v-expand-transition>
  </v-card>
  </v-col> 
  </v-row>
  <v-row cols="12" class="mb-3"></v-row>
  </v-container>
  </template>

<script>

export default {
  name: 'ServiciosComp',
  data : () =>({
    servicios: [
      {
        nombre: "Asesores Comerciales",
        photoUrl:"https://i.ibb.co/8KYGcLG/reactivate-seccion-03-01-asesores-comerciales.png"
      },
      {
        nombre: "Marketing Digital",
        photoUrl:"https://i.ibb.co/Qbf6pZB/reactivate-seccion-03-02-marketing-digital.png"
      },
      {
        nombre: "Aseoría Juridica",
        photoUrl:"https://i.ibb.co/qYYvsGQ/reactivate-seccion-03-03-asesoria-juridica.png"
      },
      {
        nombre: "Cuidado de Mascotas",
        photoUrl:"https://i.ibb.co/9ZqXcg7/reactivate-seccion-03-04-cuidado-de-mascotas.png"
      },
      {
        nombre: "Cuidado de Muebles",
        photoUrl:"https://i.ibb.co/3vxFQhW/reactivate-seccion-03-05-cuidado-de-muebles.png"
      },
      {
        nombre: "Gimnacios Entrenadores Personales",
        photoUrl:"https://i.ibb.co/hL7DfLj/reactivate-seccion-03-06-gimnasios-entrenadores-personales.png"
      },
      {
        nombre: "Arquitectura y Construcción",
        photoUrl:"https://i.ibb.co/19vHdMt/reactivate-seccion-03-07-arquitectura-construccion.png"
      },
      {
        nombre: "Asesoria Contable",
        photoUrl:"https://i.ibb.co/H7Z7k5k/reactivate-seccion-03-08-asesoria-contable.png"
      },			  
      {
        nombre: "Electricitas",
        photoUrl:"https://i.ibb.co/CVSfcNk/reactivate-seccion-03-09-electricistas.png"
      },
      {
        nombre: "Meseros Catering y Atención de Eventos",
        photoUrl:"https://i.ibb.co/PQ64Z3c/reactivate-seccion-03-10-meseros-catering-atencion-de-eventos.png"
      }			  
    ]
  }),
  }
</script>



