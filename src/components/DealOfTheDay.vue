<template>
  <div>
    <v-container>
      <v-card>
        <v-container>
          <div class="d-flex justify-center pt-3">
            <v-card width="50" class="text-center mr-3"
              ><div class="font-weight-bold">8</div>
              Hour</v-card
            >
            <div class="mt-3">:</div>
            <v-card width="50" class="text-center ml-3"
              ><div class="font-weight-bold">57</div>
              Min</v-card
            >
            <div class="ml-3 mt-3">:</div>
            <v-card width="50" class="text-center ml-3"
              ><div class="font-weight-bold">4</div>
              Sec</v-card
            >
          </div>
          <div class="mt-3">
            <div class="text-center font-weight-bold">DEAL OF THE DAY</div>
            <hr />
            <v-slide-group
              v-model="model"
              class="pa-4"
              active-class="success"
              show-arrows
            >
              <v-slide-item
                v-for="n in 15"
                :key="n"
                v-slot="{ active, toggle }"
              >
                <v-card
                  :color="active ? undefined : 'grey lighten-1'"
                  class="ma-4"
                  height="200"
                  width="630"
                  @click="toggle"
                >
                  <v-row class="fill-height" align="center" justify="center">
                    <v-scale-transition>
                      <v-icon
                        v-if="active"
                        color="white"
                        size="48"
                        v-text="'mdi-close-circle-outline'"
                      ></v-icon>
                    </v-scale-transition>
                  </v-row>
                </v-card>
              </v-slide-item>
            </v-slide-group>
          </div>
        </v-container>
      </v-card>
    </v-container>
  </div>
</template>

<script>
export default {
  data: () => ({
    model: null,
  }),
};
</script>

