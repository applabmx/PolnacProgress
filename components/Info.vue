<template>
    <v-container>
        <v-row justify="center" align="center">
            <v-col cols="12" class="main-title white--text"> SITIO EN CONSTRUCCIÓN </v-col>
            <v-col cols="12" md="6" class="info-text white--text">Estamos renovando nuestra imagen. <br>Si requieres más información comunícate a <span class="pointer text-decoration-underline" @click="OpenMail()">digital@polnac.com</span>  o si lo prefieres <br> al número 55 2585 2650 en un horario de 9:00 a 17:00 hrs. de Lunes a Viernes.</v-col>
        </v-row>
        <Contact/>
    </v-container>
</template>

<script>
export default {
    head(){
      return {
        title:`Polnac`,
        meta:[
          {
            hid:'description',
            name:'description',
            content:`Polímeros Nacionales POLNAC. Bienvenidos a nuestro sitio. Ofrecemos una amplia gama de productos y servicios`
          }
        ]
      }
    },
    methods: {
        OpenMail(){
            window.location.href = "mailto:digital@polnac.com?subject=Asunto:&body=Hola,";
        }
    },
}
</script>
<style scoped>
    .main-title{
        font-family: 'Inter';
        font-style: normal;
        font-size:24px;
        line-height: 29px;
        font-weight: 600;
        letter-spacing: 0.2em;
        text-transform: uppercase;
    }
    .info-text{
        font-family: 'Inter';
        font-style: normal;
        font-size:16px;
        line-height: 24px;
        font-weight: 400;

    }
</style>