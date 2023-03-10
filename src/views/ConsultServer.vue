<template>
<NavBarr>

  <v-card
    class="mx-auto"
    max-width="100%"
  >
    <v-container fluid>
      <v-row dense>
        <v-col
        v-for="(item, index) in items" :key="index"
          cols="3"
        >
          <v-card>
            <v-img
              :src="item.download_url"
              class="align-end"
              gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
              height="200px"
              cover
            >
              <v-card-title class="text-white" v-text="item.author"></v-card-title>
            </v-img>
          </v-card>
        </v-col>
      </v-row>
    </v-container>
  </v-card>

    <!-- <h1 class="mx-auto">card's</h1>
    <v-card
    v-for="(item, index) in items" :key="index"
    class="mx-auto"
    max-width="344"
    >
    <v-img
    :src="item.download_url"
    ></v-img>

    <v-card-title>
        <span>
            Autor: {{ item.author }}
        </span>
    </v-card-title>

    <v-card-subtitle>
        <span>
            id de la imagen: {{ item.id }}
        </span>
    </v-card-subtitle>

    <v-card-actions>    
            <v-spacer></v-spacer>
    </v-card-actions>

        <v-expand-transition>
            <div v-show="show">
                <v-divider></v-divider>

                <v-card-text>
                    
                </v-card-text>
            </div>
        </v-expand-transition>
    </v-card> -->
</NavBarr>
</template>

<script>
import { defineComponent } from 'vue';
import NavBarr from '../components/navBarr.vue';

    export default defineComponent({
        name: 'ConsultaServ',

        components: {
        NavBarr,
        },

        // data:()=>({
        //     items:[
        //     ]
        // }),

        data(){
            return{
                items:[]
            }
        },
        methods:{ //funciones
            fetchData() {
                fetch('https://picsum.photos/v2/list?page=2&limit=100',).then(response=>response.json()).then(data=>{
                    this.items=data;//como el arreglo esta ahi mismo lo llamo con this //this.item = data -items va a ser igual a un arreglo {} // this.items.push(data) -va a ser igual a [{}] //
                }) //recive varios tipos de parametros fetch, despues de la coma recibe configuracion //then se utiliza para promesas
                .catch(error => console.log(error))
            }
        },
        created(){ //ejecuciones en el created que se ejecute automaticamente abajo
            this.fetchData();
        }
    })
</script>