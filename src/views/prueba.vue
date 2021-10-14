<template>
  
</template>

<script>
import { mapGetters,mapActions } from 'vuex';
export default {


  data : () =>({
   x:{},

  }),

created: function(){
    console.log('este es ver registros')
    this.$store.dispatch('verRegistros')
},

methods:{
    list(){
        let r={}
        r=this.$store.dispatch('verRegistros')
        return r
    },
},

}


</script>


<style>

</style>