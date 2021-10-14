<template>
  <div>
      <v-stepper v-model="e1"  v-if="!isStepHidden">
        <v-stepper-header>
          <v-stepper-step :complete="e1 > 1" step="1">Sobre TI</v-stepper-step>
          <v-divider></v-divider>
          <v-stepper-step :complete="e1 > 2" step="2">Sobre tu Negocio / Servicio </v-stepper-step>
          <v-divider></v-divider>
          <v-stepper-step step="3">Categorias de tu Servicio</v-stepper-step>
        </v-stepper-header>

        <v-stepper-items>
          <v-stepper-content step="1">
          <v-form v-model="valid">
            <v-container>
                <v-row>
                  <v-col>
                      <v-alert
                      icon="mdi-account"
                      type="info"
                      text
                      >
                         <v-chip
                          class="ma-0"
                          color="orange"
                          label
                          outlined
                        >
                          {{e1}} -Completa tus datos Personales
                        </v-chip>
                      </v-alert>
                  </v-col>
                </v-row>              
              <v-row>
                <v-col
                  cols="12"
                  md="6"
                >
                  <v-text-field
                    v-model="nombre"
                    :rules="nameRules"
                    :counter="10"
                    label="Nombres"
                    outlined
                    rounded
                    required
                  ></v-text-field>
                </v-col>

                <v-col
                  cols="12"
                  md="6"
                >
                  <v-text-field
                    v-model="apellidos"
                    :rules="nameRules"
                    :counter="10"
                    label="Apellidos"
                    outlined
                    rounded                    
                    required
                  ></v-text-field>
                </v-col>
              </v-row>
              <v-row>
                <v-col
                  cols="12"
                  md="6"
                >
                  <v-text-field
                    v-model="email"
                    :rules="emailRules"
                    label="E-mail"
                    outlined
                    rounded
                    required
                  ></v-text-field>
                </v-col>
                <v-col
                  cols="12"
                  md="6"
                >
                  <v-text-field
                    v-model="telefono"
                    :rules="nameRules"
                    label="Teléfono"
                    outlined
                    rounded
                    required
                  ></v-text-field>
                </v-col>                
              </v-row>
            </v-container>
          </v-form>
          <v-btn
            color="primary"
            @click="e1 = 2"
            rounded
          >
            Continuar
          </v-btn>

          <v-btn class="ma-2" rounded @click="irAtras()">
            Atras
          </v-btn>          
          </v-stepper-content>
    
          <v-stepper-content step="2">
          <v-form v-model="valid">
            <v-container>
              <v-row>
                  <v-col>
                      <v-alert
                      icon="mdi-domain"
                      type="info"
                      text
                      >
                      {{ e1 }} -Completa la información sobre tu negocio o Servicio
                      </v-alert>
                  </v-col>
              </v-row>              
              <v-row>
                  <v-col cols=4 md=4>
                    <!-- para el logo   -->
                    <div>
                      <v-file-input
                        small-chips
                        @change="Preview_image"
                         v-model="image"
                        label="Logo para tu servicio"
                      ></v-file-input>
                    </div>
                    <v-img :src="url" max-height="150px" max-width="150px"></v-img>
                    <!-- Fin para el logo   -->
                  </v-col>
                  <v-col cols=8 md=8>
                    <v-container>
                      <!-- para los campos      -->
              <v-row>               
                  <v-col
                    cols="6"
                    md="6"
                  >
                    <v-text-field
                      v-model="companiaNombre"
                      :rules="nameRules"
                      :counter="10"
                      label="Nombre de tu Negocio o servicio"
                      outlined
                      rounded
                      required
                    ></v-text-field>
                  </v-col>
              </v-row>
              <v-row>
                <v-col
                  cols="6"
                  md="6"
                >
                  <v-text-field
                    v-model="ciudad"
                    :rules="nameRules"
                    :counter="10"
                    label="Ciudad de Residencia"
                    outlined
                    rounded                    
                    required
                  ></v-text-field>
                </v-col>
              </v-row>
              <v-row>
                <v-col
                  cols="6"
                  md="6"
                >
                  <v-text-field
                    v-model="urlServicio"
                    :rules="nameRules"
                    label="Conecta tu página Web (enlace)"
                    outlined
                    rounded
                    required
                  ></v-text-field>
                </v-col>
              </v-row>
              <v-row>
                  <v-col
                    cols="6"
                    md="6"
                  >
                    <v-text-field
                      v-model="urlFacebook"
                      :rules="nameRules"
                      label="Conecta tus red Social de Facebook (enlace)"
                      outlined
                      rounded
                      required
                    ></v-text-field>
                  </v-col>                
              </v-row>
              <v-row>
                  <v-col
                    cols="6"
                    md="6"
                  >
                    <v-text-field
                      v-model="urlInstagram"
                      :rules="nameRules"
                      label="Conecta tus red Social de Instagram (enlace)"
                      outlined
                      rounded
                      required
                    ></v-text-field>
                  </v-col>                
              </v-row>
              <v-row>
                  <v-col
                    cols="6"
                    md="6"
                  >
                  <v-alert
                    dense
                    type="info"
                  >
                  <strong>Describe tus Servicios</strong>
                  </v-alert>                
                  <v-textarea
                  v-model="descripcionServicio"
                    :rules="nameRules"                
                    class="mx-2"
                    label="Profesio, oficio con __ años de experiencia en ..."
                    outlined
                    required
                    rows="3"
                  ></v-textarea>                  
                  </v-col>                
              </v-row>   
                      <!-- Fin  para los campos -->
                    </v-container>  
                  </v-col>
              </v-row>
              <!-- -->                         
            </v-container>
          </v-form>
          <v-btn
            color="primary"
            @click="e1 = 3"
            rounded
          >
            Continuar
          </v-btn>

          <v-btn class="ma-2" rounded  @click="irAtras()">
            Atras
          </v-btn>
          </v-stepper-content>
    
          <v-stepper-content step="3">
          <v-form>
          <v-container>
          <v-row>
          <v-alert
          icon="mdi-bike"
          type="info"
          text
          >
              <v-chip
              class="ma-0"
              color="green"
              label
              outlined
            >
            <v-icon icon="mdi-cargo-ship"></v-icon>  {{e1}} -selecciona las Categorias en las que se encuentra el servico que ofreces
            </v-chip>
          </v-alert>
          </v-row>  
        <v-row>
        <v-col
          cols="12"
          sm="12"
        >
          <v-select
            v-model="selected"
            :items="this.$store.getters.getCategoriasServicios()"
            item-text="nombre"
            item-value="id"
            chips
            label="Categorias de servicio"
            multiple
            outlined
          ></v-select>
        </v-col>            
          </v-row>
          </v-container>
          </v-form>
          <v-btn
            color="success"
            @click="e1 = 1"
            rounded
          >
            Finalizar
          </v-btn>

          <v-btn class="ma-2" rounded @click="irAtras()"> 
            Atras
          </v-btn>

          </v-stepper-content>
        </v-stepper-items>
      </v-stepper>

      <!-- <v-alert icon="cloud_upload" type="info" v-if="!isLoading" >{{responsefromServer}}</v-alert> -->
  </div>
</template>


<script>
import { mapGetters } from 'vuex';
export default {
  name: 'SuscripcionesComp',
    computed: {
    ...mapGetters({getCategoriasServicios: 'getCategoriasServicios'}),
  },
  data: () => ({
      e1: 1,
      isStepHidden: false,
      url: null,
      image: null,      
      TodoBien: true,
      valid: false,
      nombre: '',
      apellidos: '',
      descripcionServicio:'',
      urlInstagram:'',
      urlFacebook:'',
      urlServicio:'',
      ciudad:'',
      companiaNombre:'',
      telefono:'',
      value: ['foo', 'bar', 'fizz', 'buzz'],
      selected:[],      
      nameRules: [
        v => !!v || 'Valor Requerido',
        v => v.length <= 10 || 'El campo no puede excer 20 carácteres',
      ],
      email: '',
      emailRules: [
        v => !!v || 'E-mail is required',
        v => /.+@.+/.test(v) || 'E-mail must be valid',
      ],

    }),

  methods: {
      Preview_image() {
      this.url= URL.createObjectURL(this.image)
    },  
    stepContinue(scope){
       if (this.TodoBien) {
          
          if (this.e1===3)
          {
            

              }
          else {
            if (this.e1==0)
            {
              this.e1 = this.e1+2;
            }
            else
            {
              this.e1++;
            }
          }

      }
        else { };
    },
    irAtras(){
      if (this.e1==1){}
    else { this.e1--}
    },

    goNextStep () {
      console.log(this.e1);
      if (this.e1===3){}
      else {this.e1++; }
    },

  },

  created: function() {
    
    //this.CategoriasServicios=this.$store.getters.getCategoriasServicios();
  },
}
</script>

<style>

</style>