<template>
  <v-container fill-height fluid class="background">
    <v-row align="center" justify="center">
      <v-col cols="12" align="center"> 
        <PolnacLogo/>
      </v-col>
      <v-col cols="12" align="center"> 
        <PlayLogo/>
      </v-col>
      <v-col cols="12" align="center">
        <Info/>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: "IndexPage",
}
</script>

<style>
  .background{
    background-image: url('./static/Background.png') ;
    -webkit-background-size: cover;
    -moz-background-size: cover;
    -o-background-size: cover;
    background-size: cover;

  }
</style>