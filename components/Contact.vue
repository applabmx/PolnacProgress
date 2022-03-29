<template>
    <v-container class="mt-15 pt-10">
        <v-row class="info-txt apps-container" algin="center" justify="center" >
            <v-col cols="12" class="white--text">Encuentra más información en nuestras redes sociales:</v-col>
            <v-col cols="2" sm="2" md="1" class="pointer"><img src="../static/linked.svg" alt="LinkedIn icono" @click="GoTo('https://www.linkedin.com/company/polnac')"> </v-col>
            <v-col cols="2" sm="2" md="1" class="pointer"><img src="../static/Facebook.svg" alt="Facebook icono" @click="GoTo('https://www.facebook.com/PolimerosNacionales')"></v-col>
            <v-col cols="2" sm="2" md="1" class="pointer"><img src="../static/Instagram.svg" alt="Instagram icono" @click="GoTo('https://www.instagram.com/polimeros_nacionales/')"></v-col>
            <v-col cols="2" sm="2" md="1" class="pointer"><img src="../static/Twitter.svg" alt="Twitter icono" @click="GoTo('https://twitter.com/PolnacOficial')"></v-col>
            <v-col cols="2" sm="2" md="1" class="pointer"><img src="../static/Youtube.svg" alt="Youtube icono"></v-col>
            <v-col cols="2" sm="2" md="1" class="pointer"><img src="../static/Whatsapp.svg" alt="Whatsapp icono" @click="OpenWhatsappMessenger()"></v-col>
        </v-row>
        <v-row class="info-txt mt-15">
            <v-col  cols="12" > Polímeros Nacionales S.A. de C.V. Lázaro Cárdenas No. 49, <br> Col. San Jerónimo Tepetlacalco, Tlalnepantla, Estado de México. C.P. 54090.</v-col>
        </v-row>
    </v-container>
</template>

<script>
export default {
    methods: {
        OpenWhatsappMessenger(){
            let android = /Android/i
            android.test(navigator.userAgent)
            let apple = /iPhone|iPad|iPod/i
            let whatsAppLink = 'https://web.whatsapp.com/send?phone=5525852650';
            //The only way safari allows to open the app is via protocol
            if ( apple.test(navigator.userAgent) ) whatsAppLink = 'whatsapp://send?phone=+5525852650';
            //Android in the other hand needs this call in order for it to work
            else if( android.test(navigator.userAgent) ) whatsAppLink = 'https://api.whatsapp.com/send?phone=5525852650';
            window.open(whatsAppLink)
        },
        GoTo(src){
            window.open(src)
        }
    },
}
</script>

<style scoped>
    .info-txt{
        font-family: 'Inter';
    }
    .apps-container{
        max-width:50%;
    }

    @media(max-width:1240px){
        .apps-container{
            max-width:100%
        }
    }
</style>