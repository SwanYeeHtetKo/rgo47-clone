<template>
  <div>
    <v-app-bar
      color="white"
      elevation="0"
    >

      <v-toolbar-title class="ml-10">
          <img src="@/assets/images/logo.png"/>
      </v-toolbar-title>

      <v-text-field label="Type for search" single-line outlined dense class="pt-5 rounded-0 ml-12 hidden-sm-and-down">
        <template v-slot:append-outer>
            <v-btn class="rounded-0 rounded-r-lg"  depressed style="margin-top:-8px;margin-left:-9px" color="#FFE12F" height="40">
                <v-icon >
                    mdi-magnify
                </v-icon>
            </v-btn>
        </template>
      </v-text-field>

      <v-spacer></v-spacer>

      <v-btn icon>
        <v-icon>mdi-account-outline</v-icon>
      </v-btn>      

      <v-menu
        left
        bottom
      >
        <template v-slot:activator="{ on, attrs }">
          <v-btn
            text
            v-bind="attrs"
            v-on="on"
          >
            My Account
          </v-btn>
        </template>

        <v-list>
          <v-list-item
            v-for="n in 5"
            :key="n"
            @click="() => {}"
          >
            <v-list-item-title>Option {{ n }}</v-list-item-title>
          </v-list-item>
        </v-list>
      </v-menu>
    
    
      <v-btn icon class="mr-3">
          <v-badge color="#FFE12F" content="6">
            <v-icon>mdi-cart-outline</v-icon>
        </v-badge>
      </v-btn>
    </v-app-bar>

    <div style="background-color:#8cc63f;" class="hidden-md-and-down">
      <v-container>
        <div class="d-flex">
                <v-btn text dark small class="mt-2">Home</v-btn>
            
            
                <v-btn text dark small class="mt-2">Offical stores</v-btn>
            
            
                <v-btn text dark small class="mt-2">Lottery</v-btn>
            
            
                <v-btn text dark small class="mt-2">Promotion Items</v-btn>
            
            
                <v-btn text dark small class="mt-2">Sell On Rgo47</v-btn>
            
            
                <v-btn text dark small class="mt-2">Free Delivery</v-btn>
            
            
                <v-btn text dark small class="mt-2">Track My Order</v-btn>
            
                <v-list-item dark style="margin-top: -10px">
                    <v-list-item-icon>
                      <v-icon style="font-size: 2rem">mdi-face-agent</v-icon>
                    </v-list-item-icon>
                    <v-list-item-content>
                        <v-list-item-title>Call us Now:</v-list-item-title>
                        <v-list-item-subtitle>09-779-999-915 / 09-779-999-928</v-list-item-subtitle>
                    </v-list-item-content>
                </v-list-item>
        </div>
      </v-container>
    </div>
  </div>
</template>