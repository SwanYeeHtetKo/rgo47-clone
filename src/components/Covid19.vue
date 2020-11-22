<template>
    <div>
        <v-container>
            <div class="d-flex">
                <div>
                    COVID-19 နှင့်သက်ဆိုင်သော ပစ္စည်းများ
                </div>
                <div class="ml-auto">
                    <p>View All</p>
                </div>
            </div>
            <hr/>
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
                  height="350"
                  width="225"
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