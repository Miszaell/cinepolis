<template>
  <v-app style="background: black">
    <v-row>
      <v-col cols="8">
        <v-row>
          <v-col>
            <v-img
              src="../../src/assets/lorax.jpg"
              width="180"
              height="280"
              class="text-center mx-lg-auto rounded-lg"
              style="border-style: ridge; border-size: 1px; border-color: white"
            />
          </v-col>
          <v-col>
            <v-img
              src="../../src/assets/dragon.jpg"
              width="180"
              height="280"
              class="text-center mx-lg-auto rounded-lg"
              style="border-style: ridge; border-size: 1px; border-color: white"
            />
          </v-col>
          <v-col>
            <v-img
              src="../../src/assets/posterGrud.png"
              width="180"
              height="280"
              class="text-center mx-lg-auto rounded-lg"
              style="border-style: ridge; border-size: 1px; border-color: white"
            />
          </v-col>
          <v-col>
            <v-img
              src="../../src/assets/posterCastillo.jpeg"
              width="180"
              height="280"
              class="text-center mx-lg-auto rounded-lg"
              style="border-style: ridge; border-size: 1px; border-color: white"
            /> </v-col
          >s
        </v-row>
        <v-row class="px-lg-5">
          <v-col style="background: white">
            <v-text>Cinépolis VIP</v-text>
          </v-col>
        </v-row>
        <v-row class="px-lg-5">
          <v-col style="background: #002069">
            <v-img
              src="../../src/assets/posterCastillo.jpeg"
              width="180"
              height="280"
              class="rounded-lg"
              style="
                border-style: ridge;
                border-size: 1px;
                border-color: white;
                margin-left: 10%;
              "
            />
          </v-col>
          <v-col style="background: #002069">
            <p style="color: white; margin-top: 80px">
              El Increíble Castillo Vagabundo
            </p>
            <p style="color: white; margin-top: 50px">13 Abril 2022</p>
          </v-col>
          <v-col style="background: #002069">
            <v-row>
              <v-btn
                rounded
                color="white"
                style="margin-top: 20%; margin-left: 30%"
                >2:00:00</v-btn
              >
            </v-row>
            <v-row>
              <v-btn color="white" style="margin-top: 30%; margin-left: 30%"
                >Comprar</v-btn
              >
            </v-row>
          </v-col>
        </v-row>
      </v-col>

      <v-col cols="4">
        <v-row
          ><v-card
            style="background: #002069"
            class="mx-auto my-lg-5"
            max-width="344"
          >
            <v-card-text>
              <v-select :items="items" label="Ciudad" solo></v-select>
              <v-select :items="items" label="Cine" solo></v-select>
            </v-card-text> </v-card
        ></v-row>
        <v-row
          ><v-card
            style="background: #002069"
            class="mx-auto my-lg-5"
            max-width="344"
          >
            <v-card-text>
              <v-slider
                v-model="value"
                step="10"
                ticks="always"
                tick-size="4"
              ></v-slider>
            </v-card-text> </v-card
        ></v-row>
        <v-row
          ><v-card
            style="background: #002069"
            class="mx-auto my-lg-5"
            max-width="344"
          >
            <v-card-text>
              <v-select :items="items" label="23 Marzo" solo></v-select>
            </v-card-text> </v-card
        ></v-row>
        <v-row
          ><v-card
            style="background: #002069"
            class="mx-auto my-lg-5"
            max-width="344"
          >
            <v-card-text>
              <p style="color: white; margin-top: 50px">Experiencia</p>
              <v-checkbox
                v-model="ex4"
                label="CINEPOLIS"
                color="white"
                dark
                hide-details
              ></v-checkbox>
              <v-checkbox
                v-model="ex4"
                label="MACRO XE"
                color="white"
                dark
                hide-details
              ></v-checkbox>
              <v-checkbox
                v-model="ex4"
                label="4 DX"
                color="white"
                dark
                hide-details
              ></v-checkbox>
              <p style="color: white; margin-top: 50px">Formato</p>
              <v-checkbox
                v-model="ex4"
                label="2D"
                color="white"
                dark
                hide-details
              ></v-checkbox>
              <v-checkbox
                v-model="ex4"
                label="3D"
                color="white"
                dark
                hide-details
              ></v-checkbox>
            </v-card-text> </v-card
        ></v-row>
      </v-col>
    </v-row>
  </v-app>
</template>
<script>
  export default {
    data () {
      return {
        value: 0,
        fruits: 0,
        ticksLabels: [
          'Figs',
          'Lemon',
          'Pear',
          'Apple',
        ],
      }
    },
  }
</script>
