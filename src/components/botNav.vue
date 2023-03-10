<template>
    <div>
        <!-- boton automatizado, al ser un for crea un btn por cada ruta (con los mostrar en los crud) -->
        <v-btn v-for="(ruta,i) in rutas" :key="i" color="success" @click="insertarRuta(ruta.ruta)" block dark ="">
        <!--key componente central(normalmente index) utilizarlo cuando haya for  -->
            <span>
                {{ ruta.nombre }}
            </span>
        </v-btn>
    </div>
</template>

<script>

export default{ //es para cuando exporte o llame este tambien adquiere todo lo que contiene dentro(todo lo del script)
    name:'botNav',

    data: ()=>({
        rutas:[
            {
                nombre:'home',
                ruta:'/'
            },
            {   
                nombre:'about',
                ruta:'/about'
            },
            {
                nombre:'help',
                ruta:'/help'
            },
            {
                nombre:'consulta',
                ruta:'/consulta'
            }
        ]
    }),

    methods: {
        insertarRuta(ruta){
            this.$router.push(ruta) //router()-route(ruta local)
        }
    },
}
</script>