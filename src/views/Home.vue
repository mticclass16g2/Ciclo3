<template>
  <div>
  <hello-world />
  <CategoriasServicioComp />
  <v-container class="blue-grey lighten-3 my-20 rounded">
  <v-row style="text-align:center;">
    <h1>¿Por qué estar en Reactivate?</h1>
 </v-row>
  <v-row>
   <v-col
    align="center"
    justify="center"    
    cols="3"
   >
    <v-img
      max-height="100"
      max-width="100"     
      src="https://i.ibb.co/thFF92c/reactivate-seccion-04-icono-01-svg.png"
     ></v-img>
   </v-col>
   <v-col
    cols="3"   
   >
     <p>Contar con perfil profesional para tu empresa</p>
   </v-col>
   <v-col
    align="center"
    justify="center"      
    cols="3"   
   >
     <v-img
      max-height="100"
      max-width="100"       
      src="https://i.ibb.co/8gHWnn2/reactivate-seccion-04-icono-02-svg.png"
     ></v-img>
   </v-col>
   <v-col
   cols="3"   
   >
     <p>Aplicar a oferta de Trabajos Disponibles</p>
   </v-col>   
 </v-row>
  <v-row>
   <v-col
    align="center"
    justify="center"   
   cols="3"
   >
     <v-img
      max-height="100"
      max-width="100"       
      src="https://i.ibb.co/BcVXt2S/reactivate-seccion-04-icono-03-svg.png"
     ></v-img>
   </v-col>
   <v-col
   cols="3" 
   >
     <p>Maximizar tu presencia y reputación en línea</p>
   </v-col>
   <v-col
    align="center"
    justify="center" 
    col2="3"  
   >
     <v-img
      src="https://i.ibb.co/w47zkQZ/reactivate-seccion-04-icono-04-svg.png"
      max-height="100"
      max-width="100"       
     ></v-img>
   </v-col>      
   <v-col
   Cols="3"
   >
     <p>Optimiza la visivilidad de tu negocio en línea</p>
   </v-col>
 </v-row>
 <v-row class="my-20"></v-row>
 </v-container>
 <v-container class="my-20 rounded">
   <p class="display-1">Contáctanos</p>
   <p class="mb-0">¿Quieres saber más de Reactívate?</p>
   <p class="mb-6">Contáctanos para brindarte toda la información que necesites</p>

  <v-row>
   <v-col
    align="center"
    justify="center"    
    cols="3"
   >
    <v-img
      max-height="100"
      max-width="100"     
      src="https://i.ibb.co/fQw4v1S/reactivate-seccion-05-icono-01-wathsapp-svg.png"
     ></v-img>
   </v-col>
   <v-col
    cols="3"   
   >
     <h3>+57 (999) 999 9999</h3>
   </v-col>
   <v-col
    align="center"
    justify="center"      
    cols="3"   
   >
     <v-img
      max-height="100"
      max-width="100"       
      src="https://i.ibb.co/kmVJfHP/reactivate-seccion-05-icono-03-linkedin-svg.png"
     ></v-img>
   </v-col>
   <v-col
   cols="3"   
   >
     <h3>síguenos</h3>
   </v-col>   
 </v-row>
  <v-row>
   <v-col
    align="center"
    justify="center"   
   cols="3"
   >
     <v-img
      max-height="100"
      max-width="100"       
      src="https://i.ibb.co/f1Yh52j/reactivate-seccion-05-icono-02-email-svg.png"
     ></v-img>
   </v-col>
   <v-col
   cols="3" 
   >
     <h3>reactivateco@outlook.com</h3>
   </v-col>
   <v-col
    align="center"
    justify="center" 
    col2="3"  
   >
     <v-img
      src="https://i.ibb.co/QrdbrY5/reactivate-seccion-05-icono-04-instagram-svg.png"
      max-height="100"
      max-width="100"       
     ></v-img>
   </v-col>      
   <v-col
   Cols="3"
   >
     <h3>síguenos</h3>
   </v-col>
 </v-row>
 <v-row class="my-20"></v-row>
 </v-container>
 </div>
</template>

<script>
  import HelloWorld from '../components/HelloWorld'
  import CategoriasServicioComp from '../components/CategoriasServicioComp'



  export default {
    name: 'Home',

    components: {
      HelloWorld,
      CategoriasServicioComp
    },
  }
</script>
<style scoped>
p {

  text-align:center;
}
</style>