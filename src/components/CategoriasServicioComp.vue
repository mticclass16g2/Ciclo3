<template>
  <v-container>
  <v-row class="text-center">
    <v-col
    v-for=" item in this.$store.getters.getCategoriasServicios()"
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
        @click="listServicioe_enCategoria(item.id)"
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
import {mapState,mapMutations,mapActions} from "vuex";

export default {
  name: 'CategoriasServicioComp',
  data : () =>({
    show: false,
  }),

  mounted: function() {
    
  },

  methods: {
    listServicioe_enCategoria(id) {
        this.$store.dispatch('setNombreCategoria',id)
        this.$store.dispatch('setIdCategoria',id)
        console.log('categoria mutada', this.$store.state.categoria)        
        this.$router.push({ name: 'servicios-categoria', params: {idCategoria:id} })     
     
      }, 
    },
    ...mapActions(['setNombreCategoria','setIdCategoria'])
  }
</script>



