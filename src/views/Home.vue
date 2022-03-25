<template>
  <v-app >
    <div style="background: black">
      <v-row>
        <v-col cols="3">
          <v-img src="../../src/assets/logo-cinepolis.png" width="270"> </v-img>
        </v-col>
        <v-col cols="9">
          <div
            class="text-right"
            style="color: white; font-size: 60px; font-weight: 500"
          >
            Estamos felices de
          </div>
          <div
            class="text-right pb-lg-5"
            style="color: white; font-size: 60px; font-weight: 500"
          >
            tenerte de vuelta
          </div>

          <div class="text-right">
            <v-row>
              <v-col>
                <v-autocomplete
                  chips
                  clearable
                  hide-details
                  hide-selected
                  item-text="name"
                  item-value="symbol"
                  label="Ubicación"
                  solo
                >
                  <template v-slot:no-data>
                    <v-list-item>
                      <v-list-item-title> Sin resultados </v-list-item-title>
                    </v-list-item>
                  </template>
                </v-autocomplete>
              </v-col>
              <v-col>
                <v-autocomplete
                  chips
                  clearable
                  hide-details
                  hide-selected
                  item-text="name"
                  item-value="symbol"
                  label="Cine"
                  solo
                >
                  <template v-slot:no-data>
                    <v-list-item>
                      <v-list-item-title> Sin resultados </v-list-item-title>
                    </v-list-item>
                  </template>
                </v-autocomplete>
              </v-col>
              <v-col>
                <v-btn to="/cartelera" block color="primary rounded-md-3">
                  Ver Cartelera
                </v-btn>
              </v-col>
            </v-row>
          </div>
        </v-col>
      </v-row>
    </div>
    <div style="background: black">
      <v-row class="pa-lg-5" style="margin-top: 5%">
        <v-carousel :show-arrows="false">
          <v-carousel-item class="rounded-lg">
            <v-img
              src="../assets/banners/bnn-1.png"
              class="rounded-lg-3"
              gradient="to top right, rgba(100,115,201,.33), rgba(25,32,72,.7)"
            />
          </v-carousel-item>
          <v-carousel-item class="rounded-lg">
            <v-img
              src="../assets/banners/bnn-1.png"
              class="rounded-lg-3"
              gradient="to top right, rgba(100,115,201,.33), rgba(25,32,72,.7)"
            />
          </v-carousel-item>
          <v-carousel-item class="rounded-lg">
            <v-img
              src="../assets/banners/bnn-1.png"
              class="rounded-lg-3"
              gradient="to top right, rgba(100,115,201,.33), rgba(25,32,72,.7)"
            />
          </v-carousel-item>
          <v-carousel-item class="rounded-lg">
            <v-img
              src="../assets/banners/bnn-1.png"
              class="rounded-lg-3"
              gradient="to top right, rgba(100,115,201,.33), rgba(25,32,72,.7)"
            />
          </v-carousel-item>
        </v-carousel>
      </v-row>
    </div>
    <div style="background: black">
      <p style="color: white; font-size: 30px; font-weight: lighter">
        Estrenos
      </p>
      <v-row class="d-flex align-center">
        <v-col
          ><v-img
            src="../../src/assets/lorax.jpg"
            class="mx-lg-auto rounded-lg"
            style="border-style: ridge; border-size: 1px; border-color: white"
            width="280"
            height="380"
        /></v-col>
        <v-col>
          <v-img
            src="../../src/assets/dragon.jpg"
            class="mx-lg-auto rounded-lg"
            style="border-style: ridge; border-size: 1px; border-color: white"
            width="280"
            height="380"
          />
        </v-col>
        <v-col>
          <v-img
            src="../../src/assets/posterGrud.png"
            width="280"
            class="mx-lg-auto rounded-lg"
            style="border-style: ridge; border-size: 1px; border-color: white"
            height="380"
          />
        </v-col>
        <v-col>
          <v-img
            src="../../src/assets/posterCastillo.jpeg"
            width="280"
            class="mx-lg-auto rounded-lg"
            style="border-style: ridge; border-size: 1px; border-color: white"
            height="380"
          />
        </v-col>
      </v-row>
    </div>
     <div style="background: black">
      <p style="color: white; font-size: 30px; font-weight: lighter; margin-top:5%">
        Proximamente
      </p>
      <v-row class="d-flex align-center">
        <v-col
          ><v-img
            src="../../src/assets/lorax.jpg"
            class="mx-lg-auto rounded-lg"
            style="border-style: ridge; border-size: 1px; border-color: white"
            width="280"
            height="380"
        /></v-col>
        <v-col>
          <v-img
            src="../../src/assets/dragon.jpg"
            class="mx-lg-auto rounded-lg"
            style="border-style: ridge; border-size: 1px; border-color: white"
            width="280"
            height="380"
          />
        </v-col>
        <v-col>
          <v-img
            src="../../src/assets/posterGrud.png"
            width="280"
            class="mx-lg-auto rounded-lg"
            style="border-style: ridge; border-size: 1px; border-color: white"
            height="380"
          />
        </v-col>
        <v-col>
          <v-img
            src="../../src/assets/posterCastillo.jpeg"
            width="280"
            class="mx-lg-auto rounded-lg"
            style="border-style: ridge; border-size: 1px; border-color: white"
            height="380"
          />
        </v-col>
      </v-row>
    </div>
  </v-app>
</template>

<script>
  export default {
    name: "Home",
    data() {
      return {};
    },
  };
</script>
