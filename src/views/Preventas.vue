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
        <v-row class="px-lg-5 mt-lg-10">
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
          <v-card class="mx-auto my-lg-5" max-width="344" color="#002069">
            <v-card>
              <v-card-title>
                <v-icon>mdi-map-marker-radius-outline</v-icon>
                Complejos
              </v-card-title>
            </v-card>
            <v-card-text>
              <v-autocomplete
                chips
                clearable
                hide-details
                hide-selected
                item-text="name"
                item-value="symbol"
                label="Ubicación"
                class="my-lg-3"
                solo
              >
                <template v-slot:no-data>
                  <v-list-item>
                    <v-list-item-title> Sin resultados </v-list-item-title>
                  </v-list-item>
                </template>
              </v-autocomplete>
              <v-autocomplete
                chips
                clearable
                hide-details
                hide-selected
                item-text="name"
                item-value="symbol"
                label="Cine"
                class="my-lg-3"
                solo
              >
                <template v-slot:no-data>
                  <v-list-item>
                    <v-list-item-title> Sin resultados </v-list-item-title>
                  </v-list-item>
                </template>
              </v-autocomplete>
            </v-card-text>
          </v-card>
          <v-card class="mx-auto my-lg-5" max-width="344" color="#002069">
            <v-card>
              <v-card-title>
                <v-icon>mdi-clock-time-five-outline</v-icon>
                Horario
              </v-card-title>
            </v-card>
            <v-card-text class="text-center">
              <v-slider
                v-model="value"
                step="10"
                ticks="always"
                color="white"
                tick-size="4"
              ></v-slider>
              <v-subheader dark class="mx-lg-auto text-center"
                >00:00:00 - 00:00:00</v-subheader
              >
            </v-card-text>
          </v-card>
          <v-card class="mx-auto my-lg-5" max-width="344" color="#002069">
            <v-card>
              <v-card-title>
                <v-icon>mdi-calendar-blank-outline</v-icon>
                Día
              </v-card-title>
            </v-card>
            <v-card-text>
              <v-menu
                ref="menu"
                v-model="menu2"
                :close-on-content-click="false"
                :nudge-right="40"
                :return-value.sync="time"
                transition="scale-transition"
                offset-y
                dark
                max-width="290px"
                min-width="290px"
              >
                <template v-slot:activator="{ on, attrs }">
                  <v-text-field
                    v-model="time"
                    label="Picker in menu"
                    prepend-icon="mdi-clock-time-four-outline"
                    readonly
                    dark
                    v-bind="attrs"
                    v-on="on"
                  ></v-text-field>
                </template>
                <v-time-picker
                  v-if="menu2"
                  v-model="time"
                  full-width
                  @click:minute="$refs.menu.save(time)"
                ></v-time-picker>
              </v-menu>
            </v-card-text>
          </v-card>
          <v-card class="mx-auto my-lg-5" max-width="344" color="#002069">
            <v-card>
              <v-card-title>
                <v-icon>mdi-movie</v-icon>
                Tipo de proyección
              </v-card-title>
            </v-card>
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
            </v-card-text>
          </v-card>
      </v-col>
    </v-row>
  </v-app>
</template>
<script>
  export default {
    data() {
      return {
        value: 0,
        fruits: 0,
        ticksLabels: ["Figs", "Lemon", "Pear", "Apple"],
      };
    },
  };
</script>
