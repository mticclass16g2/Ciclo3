<template>
  <div>
  <v-card
    :loading="loading"
    class="mx-auto my-12"
    max-width="374"
  >
    <template slot="progress">
      <v-progress-linear
        color="deep-purple"
        height=10
        indeterminate
      ></v-progress-linear>
    </template>
    <v-img
      height="250"
      :src="service[0].imageUrl"
    ></v-img>

    <v-card-title>{{service[0].companyName}}</v-card-title>

    <v-card-text>
      <v-row
        align="center"
        class="mx-0"
      >
        <v-rating
          :value="4.5"
          color="amber"
          dense
          half-increments
          readonly
          size="14"
        ></v-rating>

        <div class="grey--text ms-4">
          4.5 (413)
        </div>
      </v-row>

      <div class="my-4 text-subtitle-1">
         • Categoria.., item
      </div>

      <div>{{service[0].descripcion}}</div>
    </v-card-text>

    <v-divider class="mx-4"></v-divider>

    <v-card-title>Contacto</v-card-title>

    <v-card-text>
    <v-list>
      <template v-for="item in contacItems"
      >
        <v-list-item 
        :key="item.icon">
          <v-list-item-avatar>
            <v-icon
              v-text="item.icon"
            ></v-icon>
          </v-list-item-avatar>
          <v-list-item-title v-text="item.text + ': ' + item.valor"></v-list-item-title>
        </v-list-item>
      </template>
    </v-list>
    </v-card-text>

    <v-card-actions>
      <v-btn
        color="deep-purple lighten-2"
        text
        @click="reserve"
      >
        Contactar
      </v-btn>
    </v-card-actions>
  </v-card>
  </div>
</template>
<script>
  export default {

    data: () => ({
      serviciosCategoria:[],
      loading: false,
      selection: 1,
      service:[],
      contacItems:[],      
    }),
    created() {
    
      this.Initialize()
      this.service=this.getService(this.$route.params.idServicio);
      console.log('este es service:', this.service)
      this.contacItems=[
            {
              text: 'Persona de Contacto',
              icon: 'mdi-account',
              valor: this.service[0].contacto
            },
            {
              text: 'Telefono',
              icon: 'mdi-phone-classic',              
              valor: this.service[0].telefono

            },
            {
              text: 'email',
              icon: 'mdi-email',
              valor: this.service[0].email
            }
      ]      

    },
    methods: {
      reserve () {
        this.loading = true

        setTimeout(() => (this.loading = false), 2000)
      },
      Initialize (){
this.serviciosCategoria= [
        {
            id: 1,
            companyName: 'Compañía 1',
            descripcion: 'Descripcion 1',
            imageUrl: 'https://cdn.vuetifyjs.com/images/cards/cooking.png',
            contacto: 'Persona 1',
            telefono: 'Teléfono 1',
            email: 'xx1@gmail.com',
            idCategoria: 8
        },
        {
            id: 2,
            companyName: 'Compañía 2',
            descripcion: 'Descripcion 2',
            imageUrl: 'https://cdn.vuetifyjs.com/images/cards/cooking.png',
            contacto: 'Persona 2',
            telefono: 'Teléfono 2',
            email: 'xx2@gmail.com',
            idCategoria: 9
        },
        {
            id: 3,
            companyName: 'Compañía 3',
            descripcion: 'Descripcion 3',
            imageUrl: 'https://cdn.vuetifyjs.com/images/cards/cooking.png',
            contacto: 'Persona 3',
            telefono: 'Teléfono 3',
            email: 'xx3@gmail.com',
            idCategoria: 5
        },
        {
            id: 4,
            companyName: 'Compañía 4',
            descripcion: 'Descripcion 4',
            imageUrl: 'https://cdn.vuetifyjs.com/images/cards/cooking.png',
            contacto: 'Persona 4',
            telefono: 'Teléfono 4',
            email: 'xx4@gmail.com',
            idCategoria: 4
        },
        {
            id: 5,
            companyName: 'Compañía 5',
            descripcion: 'Descripcion 5',
            imageUrl: 'https://cdn.vuetifyjs.com/images/cards/cooking.png',
            contacto: 'Persona 5',
            telefono: 'Teléfono 5',
            email: 'xx5@gmail.com',
            idCategoria: 8
        },
        {
            id: 6,
            companyName: 'Compañía 6',
            descripcion: 'Descripcion 6',
            imageUrl: 'https://cdn.vuetifyjs.com/images/cards/cooking.png',
            contacto: 'Persona 6',
            telefono: 'Teléfono 6',
            email: 'xx6@gmail.com',
            idCategoria: 7
        },
        {
            id: 7,
            companyName: 'Compañía 7',
            descripcion: 'Descripcion 7',
            imageUrl: 'https://cdn.vuetifyjs.com/images/cards/cooking.png',
            contacto: 'Persona 7',
            telefono: 'Teléfono 7',
            email: 'xx7@gmail.com',
            idCategoria: 2
        },
        {
            id: 8,
            companyName: 'Compañía 8',
            descripcion: 'Descripcion 8',
            imageUrl: 'https://cdn.vuetifyjs.com/images/cards/cooking.png',
            contacto: 'Persona 8',
            telefono: 'Teléfono 8',
            email: 'xx8@gmail.com',
            idCategoria: 6
        },
        {
            id: 9,
            companyName: 'Compañía 9',
            descripcion: 'Descripcion 9',
            imageUrl: 'https://cdn.vuetifyjs.com/images/cards/cooking.png',
            contacto: 'Persona 9',
            telefono: 'Teléfono 9',
            email: 'xx9@gmail.com',
            idCategoria: 5
        },
        {
            id: 10,
            companyName: 'Compañía 10',
            descripcion: 'Descripcion 10',
            imageUrl: 'https://cdn.vuetifyjs.com/images/cards/cooking.png',
            contacto: 'Persona 10',
            telefono: 'Teléfono 10',
            email: 'xx10@gmail.com',
            idCategoria: 8
        },
        {
            id: 11,
            companyName: 'Compañía 11',
            descripcion: 'Descripcion 11',
            imageUrl: 'https://cdn.vuetifyjs.com/images/cards/cooking.png',
            contacto: 'Persona 11',
            telefono: 'Teléfono 11',
            email: 'xx11@gmail.com',
            idCategoria: 1
        },
        {
            id: 12,
            companyName: 'Compañía 12',
            descripcion: 'Descripcion 12',
            imageUrl: 'https://cdn.vuetifyjs.com/images/cards/cooking.png',
            contacto: 'Persona 12',
            telefono: 'Teléfono 12',
            email: 'xx12@gmail.com',
            idCategoria: 9
        },
        {
            id: 13,
            companyName: 'Compañía 13',
            descripcion: 'Descripcion 13',
            imageUrl: 'https://cdn.vuetifyjs.com/images/cards/cooking.png',
            contacto: 'Persona 13',
            telefono: 'Teléfono 13',
            email: 'xx13@gmail.com',
            idCategoria: 5
        },
        {
            id: 14,
            companyName: 'Compañía 14',
            descripcion: 'Descripcion 14',
            imageUrl: 'https://cdn.vuetifyjs.com/images/cards/cooking.png',
            contacto: 'Persona 14',
            telefono: 'Teléfono 14',
            email: 'xx14@gmail.com',
            idCategoria: 10
        },
        {
            id: 15,
            companyName: 'Compañía 15',
            descripcion: 'Descripcion 15',
            imageUrl: 'https://cdn.vuetifyjs.com/images/cards/cooking.png',
            contacto: 'Persona 15',
            telefono: 'Teléfono 15',
            email: 'xx15@gmail.com',
            idCategoria: 10
        },
        {
            id: 16,
            companyName: 'Compañía 16',
            descripcion: 'Descripcion 16',
            imageUrl: 'https://cdn.vuetifyjs.com/images/cards/cooking.png',
            contacto: 'Persona 16',
            telefono: 'Teléfono 16',
            email: 'xx16@gmail.com',
            idCategoria: 1
        },
        {
            id: 17,
            companyName: 'Compañía 17',
            descripcion: 'Descripcion 17',
            imageUrl: 'https://cdn.vuetifyjs.com/images/cards/cooking.png',
            contacto: 'Persona 17',
            telefono: 'Teléfono 17',
            email: 'xx17@gmail.com',
            idCategoria: 6
        },
        {
            id: 18,
            companyName: 'Compañía 18',
            descripcion: 'Descripcion 18',
            imageUrl: 'https://cdn.vuetifyjs.com/images/cards/cooking.png',
            contacto: 'Persona 18',
            telefono: 'Teléfono 18',
            email: 'xx18@gmail.com',
            idCategoria: 1
        },
        {
            id: 19,
            companyName: 'Compañía 19',
            descripcion: 'Descripcion 19',
            imageUrl: 'https://cdn.vuetifyjs.com/images/cards/cooking.png',
            contacto: 'Persona 19',
            telefono: 'Teléfono 19',
            email: 'xx19@gmail.com',
            idCategoria: 10
        },
        {
            id: 20,
            companyName: 'Compañía 20',
            descripcion: 'Descripcion 20',
            imageUrl: 'https://cdn.vuetifyjs.com/images/cards/cooking.png',
            contacto: 'Persona 20',
            telefono: 'Teléfono 20',
            email: 'xx20@gmail.com',
            idCategoria: 8
        },
        {
            id: 21,
            companyName: 'Compañía 21',
            descripcion: 'Descripcion 21',
            imageUrl: 'https://cdn.vuetifyjs.com/images/cards/cooking.png',
            contacto: 'Persona 21',
            telefono: 'Teléfono 21',
            email: 'xx21@gmail.com',
            idCategoria: 2
        },
        {
            id: 22,
            companyName: 'Compañía 22',
            descripcion: 'Descripcion 22',
            imageUrl: 'https://cdn.vuetifyjs.com/images/cards/cooking.png',
            contacto: 'Persona 22',
            telefono: 'Teléfono 22',
            email: 'xx22@gmail.com',
            idCategoria: 3
        },
        {
            id: 23,
            companyName: 'Compañía 23',
            descripcion: 'Descripcion 23',
            imageUrl: 'https://cdn.vuetifyjs.com/images/cards/cooking.png',
            contacto: 'Persona 23',
            telefono: 'Teléfono 23',
            email: 'xx23@gmail.com',
            idCategoria: 9
        },
        {
            id: 24,
            companyName: 'Compañía 24',
            descripcion: 'Descripcion 24',
            imageUrl: 'https://cdn.vuetifyjs.com/images/cards/cooking.png',
            contacto: 'Persona 24',
            telefono: 'Teléfono 24',
            email: 'xx24@gmail.com',
            idCategoria: 1
        },
        {
            id: 25,
            companyName: 'Compañía 25',
            descripcion: 'Descripcion 25',
            imageUrl: 'https://cdn.vuetifyjs.com/images/cards/cooking.png',
            contacto: 'Persona 25',
            telefono: 'Teléfono 25',
            email: 'xx25@gmail.com',
            idCategoria: 1
        },
        {
            id: 26,
            companyName: 'Compañía 26',
            descripcion: 'Descripcion 26',
            imageUrl: 'https://cdn.vuetifyjs.com/images/cards/cooking.png',
            contacto: 'Persona 26',
            telefono: 'Teléfono 26',
            email: 'xx26@gmail.com',
            idCategoria: 4
        },
        {
            id: 27,
            companyName: 'Compañía 27',
            descripcion: 'Descripcion 27',
            imageUrl: 'https://cdn.vuetifyjs.com/images/cards/cooking.png',
            contacto: 'Persona 27',
            telefono: 'Teléfono 27',
            email: 'xx27@gmail.com',
            idCategoria: 10
        },
        {
            id: 28,
            companyName: 'Compañía 28',
            descripcion: 'Descripcion 28',
            imageUrl: 'https://cdn.vuetifyjs.com/images/cards/cooking.png',
            contacto: 'Persona 28',
            telefono: 'Teléfono 28',
            email: 'xx28@gmail.com',
            idCategoria: 3
        },
        {
            id: 29,
            companyName: 'Compañía 29',
            descripcion: 'Descripcion 29',
            imageUrl: 'https://cdn.vuetifyjs.com/images/cards/cooking.png',
            contacto: 'Persona 29',
            telefono: 'Teléfono 29',
            email: 'xx29@gmail.com',
            idCategoria: 8
        },
        {
            id: 30,
            companyName: 'Compañía 30',
            descripcion: 'Descripcion 30',
            imageUrl: 'https://cdn.vuetifyjs.com/images/cards/cooking.png',
            contacto: 'Persona 30',
            telefono: 'Teléfono 30',
            email: 'xx30@gmail.com',
            idCategoria: 8
        },
        {
            id: 31,
            companyName: 'Compañía 31',
            descripcion: 'Descripcion 31',
            imageUrl: 'https://cdn.vuetifyjs.com/images/cards/cooking.png',
            contacto: 'Persona 31',
            telefono: 'Teléfono 31',
            email: 'xx31@gmail.com',
            idCategoria: 5
        },
        {
            id: 32,
            companyName: 'Compañía 32',
            descripcion: 'Descripcion 32',
            imageUrl: 'https://cdn.vuetifyjs.com/images/cards/cooking.png',
            contacto: 'Persona 32',
            telefono: 'Teléfono 32',
            email: 'xx32@gmail.com',
            idCategoria: 6
        },
        {
            id: 33,
            companyName: 'Compañía 33',
            descripcion: 'Descripcion 33',
            imageUrl: 'https://cdn.vuetifyjs.com/images/cards/cooking.png',
            contacto: 'Persona 33',
            telefono: 'Teléfono 33',
            email: 'xx33@gmail.com',
            idCategoria: 2
        },
        {
            id: 34,
            companyName: 'Compañía 34',
            descripcion: 'Descripcion 34',
            imageUrl: 'https://cdn.vuetifyjs.com/images/cards/cooking.png',
            contacto: 'Persona 34',
            telefono: 'Teléfono 34',
            email: 'xx34@gmail.com',
            idCategoria: 3
        },
        {
            id: 35,
            companyName: 'Compañía 35',
            descripcion: 'Descripcion 35',
            imageUrl: 'https://cdn.vuetifyjs.com/images/cards/cooking.png',
            contacto: 'Persona 35',
            telefono: 'Teléfono 35',
            email: 'xx35@gmail.com',
            idCategoria: 6
        },
        {
            id: 36,
            companyName: 'Compañía 36',
            descripcion: 'Descripcion 36',
            imageUrl: 'https://cdn.vuetifyjs.com/images/cards/cooking.png',
            contacto: 'Persona 36',
            telefono: 'Teléfono 36',
            email: 'xx36@gmail.com',
            idCategoria: 9
        },
        {
            id: 37,
            companyName: 'Compañía 37',
            descripcion: 'Descripcion 37',
            imageUrl: 'https://cdn.vuetifyjs.com/images/cards/cooking.png',
            contacto: 'Persona 37',
            telefono: 'Teléfono 37',
            email: 'xx37@gmail.com',
            idCategoria: 4
        },
        {
            id: 38,
            companyName: 'Compañía 38',
            descripcion: 'Descripcion 38',
            imageUrl: 'https://cdn.vuetifyjs.com/images/cards/cooking.png',
            contacto: 'Persona 38',
            telefono: 'Teléfono 38',
            email: 'xx38@gmail.com',
            idCategoria: 7
        },
        {
            id: 39,
            companyName: 'Compañía 39',
            descripcion: 'Descripcion 39',
            imageUrl: 'https://cdn.vuetifyjs.com/images/cards/cooking.png',
            contacto: 'Persona 39',
            telefono: 'Teléfono 39',
            email: 'xx39@gmail.com',
            idCategoria: 8
        },
        {
            id: 40,
            companyName: 'Compañía 40',
            descripcion: 'Descripcion 40',
            imageUrl: 'https://cdn.vuetifyjs.com/images/cards/cooking.png',
            contacto: 'Persona 40',
            telefono: 'Teléfono 40',
            email: 'xx40@gmail.com',
            idCategoria: 3
        },
        {
            id: 41,
            companyName: 'Compañía 41',
            descripcion: 'Descripcion 41',
            imageUrl: 'https://cdn.vuetifyjs.com/images/cards/cooking.png',
            contacto: 'Persona 41',
            telefono: 'Teléfono 41',
            email: 'xx41@gmail.com',
            idCategoria: 8
        },
        {
            id: 42,
            companyName: 'Compañía 42',
            descripcion: 'Descripcion 42',
            imageUrl: 'https://cdn.vuetifyjs.com/images/cards/cooking.png',
            contacto: 'Persona 42',
            telefono: 'Teléfono 42',
            email: 'xx42@gmail.com',
            idCategoria: 4
        },
        {
            id: 43,
            companyName: 'Compañía 43',
            descripcion: 'Descripcion 43',
            imageUrl: 'https://cdn.vuetifyjs.com/images/cards/cooking.png',
            contacto: 'Persona 43',
            telefono: 'Teléfono 43',
            email: 'xx43@gmail.com',
            idCategoria: 9
        },
        {
            id: 44,
            companyName: 'Compañía 44',
            descripcion: 'Descripcion 44',
            imageUrl: 'https://cdn.vuetifyjs.com/images/cards/cooking.png',
            contacto: 'Persona 44',
            telefono: 'Teléfono 44',
            email: 'xx44@gmail.com',
            idCategoria: 9
        },
        {
            id: 45,
            companyName: 'Compañía 45',
            descripcion: 'Descripcion 45',
            imageUrl: 'https://cdn.vuetifyjs.com/images/cards/cooking.png',
            contacto: 'Persona 45',
            telefono: 'Teléfono 45',
            email: 'xx45@gmail.com',
            idCategoria: 10
        },
        {
            id: 46,
            companyName: 'Compañía 46',
            descripcion: 'Descripcion 46',
            imageUrl: 'https://cdn.vuetifyjs.com/images/cards/cooking.png',
            contacto: 'Persona 46',
            telefono: 'Teléfono 46',
            email: 'xx46@gmail.com',
            idCategoria: 10
        },
        {
            id: 47,
            companyName: 'Compañía 47',
            descripcion: 'Descripcion 47',
            imageUrl: 'https://cdn.vuetifyjs.com/images/cards/cooking.png',
            contacto: 'Persona 47',
            telefono: 'Teléfono 47',
            email: 'xx47@gmail.com',
            idCategoria: 7
        },
        {
            id: 48,
            companyName: 'Compañía 48',
            descripcion: 'Descripcion 48',
            imageUrl: 'https://cdn.vuetifyjs.com/images/cards/cooking.png',
            contacto: 'Persona 48',
            telefono: 'Teléfono 48',
            email: 'xx48@gmail.com',
            idCategoria: 5
        },
        {
            id: 49,
            companyName: 'Compañía 49',
            descripcion: 'Descripcion 49',
            imageUrl: 'https://cdn.vuetifyjs.com/images/cards/cooking.png',
            contacto: 'Persona 49',
            telefono: 'Teléfono 49',
            email: 'xx49@gmail.com',
            idCategoria: 10
        },
        {
            id: 50,
            companyName: 'Compañía 50',
            descripcion: 'Descripcion 50',
            imageUrl: 'https://cdn.vuetifyjs.com/images/cards/cooking.png',
            contacto: 'Persona 50',
            telefono: 'Teléfono 50',
            email: 'xx50@gmail.com',
            idCategoria: 10
        }
      ]
         

    },
    getService (idServicio) {
        //console.log('id:',id)
        this.service = [];
        console.log('este es servicios categoria:',this.serviciosCategoria[0]) 
        const r=this.serviciosCategoria.filter(function(x) {return x.id==idServicio;})
        //this.service=r
        console.log('este es r:',r) 
        return r       
        //if(r !==null ){
          //  this.service=r; 
        //} else {
        //    this.service =null;
        //}

      },
    },
  }
</script>