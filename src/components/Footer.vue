<template>
    <div>
        <v-container>
            <v-row>
                <v-col cols="12" xs="12" sm="12" md="4" lg="3">
                    <v-card class="text-center" width="255"  elevation="0" color="#454545">
                        <v-card-text>
                            <div style="color:#A5A5A5" class="font-weight-bold">CUSTOMER SERVICE</div>
                            <div style="color:#A5A5A5" class="font-weight-bold">HOTLINE:</div>
                            <div style="color:#EBD02C" class="font-weight-bold">09-779-999-915</div>
                            <div style="color:#EBD02C" class="font-weight-bold">09-779-999-928</div>
                            <div style="color:#EBD02C" class="font-weight-bold">09-779-999-941</div>
                            <div style="color:#EBD02C" class="font-weight-bold">09-779-999-906</div>
                            <hr class="mt-5"/>
                            <p class="white--text mt-5 font-weight-bold">SECURE PAYMENT</p>
                            <v-img src="@/assets/images/pays-for-rgo.png" width="200" height="80"/>
                        </v-card-text>
                    </v-card>
                </v-col>

                <v-col cols="12" xs="12" sm="12" md="4" lg="2">
                    <p class="font-weight-black">ABOUT</p>
                    <p class="font-weight-medium" style="color:#A5A5A5">Contact Us</p>
                    <p class="font-weight-medium" style="color:#A5A5A5">Merchant Application Form</p>
                    <p class="font-weight-medium" style="color:#A5A5A5">Careers</p>
                    <p class="font-weight-medium" style="color:#A5A5A5">Clear Cache</p>
                </v-col>

                <v-col cols="12" xs="12" sm="12" md="4" lg="2">
                    <p class="font-weight-black">POLICY</p>
                    <p class="font-weight-medium" style="color:#A5A5A5">Privacy</p>
                </v-col>

                <v-col cols="12" xs="12" sm="12" md="4" lg="2">
                    <p class="font-weight-black">SOCIAL</p>
                    <p class="font-weight-medium" style="color:#A5A5A5">Facebook</p>
                    <p class="font-weight-medium" style="color:#A5A5A5">Instagram</p>
                    <p class="font-weight-medium" style="color:#A5A5A5">YouTube</p>
                </v-col>
                    
                <v-col cols="12" xs="12" sm="12" md="4" lg="3">
                    <p class="font-weight-black">OUR OFFICIAL FACEBOOK PAGE</p>
                    <v-img contain src="@/assets/images/Official-Page.png"/>
                </v-col>
            </v-row>
            <hr/>
            <p class="mt-5">Copyright &copy; <span style="color:#7CDF48">rgo47</span> . All Rights Reserved</p>
        </v-container>
        <v-btn
        fab
        small
        dark
        bottom
        fixed
        left
        color="#7CDF48"
      >
        <v-icon>mdi-bell-alert-outline</v-icon>
      </v-btn>

      <v-btn
        fab
        dark
        fixed
        bottom
        right
        color="#fff"
        style="margin-right: 4rem"
      >
        <v-img width="20" height="40" contain src="@/assets/images/facebook-messenger-small.png"/>
      </v-btn>

      <v-btn
        fixed
        fab
        dark
        small        
        bottom
        right
        color="#7CDF48"
        @click="$vuetify.goTo(target, options)"
        v-show="fab"
        v-scroll="onScroll"
      >
        <v-icon>mdi-chevron-up</v-icon>
      </v-btn>
    </div>
</template>

<script>
import * as easings from 'vuetify/es5/services/goto/easing-patterns'
export default {
    data () {
      return {
        type: 'number',
        number: 0,
        duration: 1000,
        offset: 0,
        easing: 'easeInOutCubic',
        easings: Object.keys(easings),
        fab: false
      }
    },

    computed: {
      target () {
        const value = this[this.type]
        if (!isNaN(value)) return Number(value)
        else return value
      },
      options () {
        return {
          duration: this.duration,
          offset: this.offset,
          easing: this.easing,
        }
      },
    },

    methods:{
      onScroll (e) {
      if (typeof window === 'undefined') return
      const top = window.pageYOffset ||   e.target.scrollTop || 0
      this.fab = top > 20
    },
    toTop () {
      this.$vuetify.goTo(0)
    }
    }
}
</script>