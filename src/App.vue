<template>
  <v-app style="font-family: 'montserrat'; background: black">
    <v-app-bar app color="#000000" dark class="pa-md-5">
      <div class="d-flex align-center" style="cursor:pointer;" @click="$router.push({path:'/'})">
        <v-img
          alt="Logo"
          class="shrink mr-2"
          contain
          src="../src/assets/log.png"
          transition="scale-transition"
          width="180"
        />
      </div>

      <v-spacer></v-spacer>
      <v-btn text> Promociones </v-btn>
      <v-btn text> Próximos estrenos </v-btn>
      <v-btn text to="/preve"> Preventas </v-btn>
      <v-btn text> Más </v-btn>
    </v-app-bar>

    <v-main
      style="
        padding-top: 6%;
        padding-right: 3%;
        padding-left: 3%;
        background: black;
      "
    >
      <router-view />
    </v-main>
    <v-footer color="#002069" dark class="mt-lg-8">
      <v-col class="text-center" cols="4">
        <strong class="mb-5">Quienes somos</strong>
        <p class="body-2">Proveedores</p>
        <p class="body-2">Trabaja en Cinépolis</p>
        <p class="body-2">Próximas aperturas</p>
        <p class="body-2">Ventas corporativo</p>
      </v-col>
      <v-col class="text-center" cols="4">
        <strong class="mb-5">Legales</strong>
        <p class="body-2">Términos y condiciones</p>
        <p class="body-2">Aviso de privacidad</p>
        <p class="body-2">Términos Cinecash</p>
        <p class="body-2">Términos y condiciones Cineticket</p>
        <p class="body-2">Código de conducta</p>
      </v-col>
      <v-col class="text-center" cols="4">
        <strong class="mb-5">Contacto</strong>
        <p class="body-2">Facturación electrónica</p>
        <p class="body-2">Dejanos tus comantarios</p>
        <p class="body-2">512 122 60 60</p>
      </v-col>
    </v-footer>
  </v-app>
</template>

<script>
  export default {
    name: "App",

    data: () => ({
      //
    }),
  };
</script>

<style scoped>
  .v-app {
    font-family: "Montserrat";
  }
</style>
