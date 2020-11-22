<template>
    <div class="banner">
        <v-container >
        <v-row>
            <v-col cols="12" xs="12" sm="12" md="12" lg="3">
            <v-card
                width="100%"
            >
            <v-toolbar
                color="#8CC63F"
                dark
                dense
                elevation="0"
            >
                <v-app-bar-nav-icon></v-app-bar-nav-icon>

                <v-toolbar-title>ALL CATEGORIES</v-toolbar-title>
            </v-toolbar>
                <v-list dense>

                <v-list-group  v-for="(item,i) in categories" :key="i">
                    <template v-slot:activator>
                    <v-list-item-icon>
                        <v-img width="20" :src="item.image"/>
                    </v-list-item-icon>
                    <v-list-item-title>{{item.name}}</v-list-item-title>
                    </template>

                    <v-list-group
                    no-action
                    sub-group
                    >
                    <template v-slot:activator>
                        <v-list-item-content>
                        <v-list-item-title>TOPS & SETS</v-list-item-title>
                        </v-list-item-content>
                    </template>

                    <v-list-item
                        v-for="([title, icon], i) in admins"
                        :key="i"
                        link
                    >
                        <v-list-item-title v-text="title"></v-list-item-title>

                        <v-list-item-icon>
                        <v-icon v-text="icon"></v-icon>
                        </v-list-item-icon>
                    </v-list-item>
                    </v-list-group>

                    <v-list-group
                    no-action
                    sub-group
                    >
                    <template v-slot:activator>
                        <v-list-item-content>
                        <v-list-item-title>Actions</v-list-item-title>
                        </v-list-item-content>
                    </template>

                    <v-list-item
                        v-for="([title, icon], i) in cruds"
                        :key="i"
                        link
                    >
                        <v-list-item-title v-text="title"></v-list-item-title>

                        <v-list-item-icon>
                        <v-icon v-text="icon"></v-icon>
                        </v-list-item-icon>
                    </v-list-item>
                    </v-list-group>
                </v-list-group>
                
                </v-list>
            </v-card>
            </v-col>
            <v-col cols="12" xs="12" sm="12" md="12" lg="9">
            <v-carousel height="300" hide-delimiter-background="true">
                <v-carousel-item
                contain
                v-for="(item,i) in carousel"
                :key="i"
                :src="item.src"
                reverse-transition="fade-transition"
                transition="fade-transition"
                ></v-carousel-item>
            </v-carousel>

            <div class="d-flex mt-5">
                <v-img src="@/assets/images/b0qTW24804.jpg" contain width="223" height="197"/>
                <v-img src="@/assets/images/ulsaP22612.jpg" contain width="223" height="197"/>
            </div>
            </v-col>
        </v-row>
        </v-container>
    </div>
</template>

<script>
export default {
    data:() => ({
        admins: [
        ['Management', 'mdi-account-multiple-outline'],
        ['Settings', 'mdi-cog-outline'],
      ],
      cruds: [
        ['Create', 'mdi-plus-outline'],
        ['Read', 'mdi-file-outline'],
        ['Update', 'mdi-update'],
        ['Delete', 'mdi-delete'],
      ],
      carousel:[
        {
            src: require(`@/assets/images/7PFjb09409.webp`),
          },
          {
            src: require(`@/assets/images/sTMAd10407.jpg`),
          },
          {
            src: require(`@/assets/images/2HDUB06705.jpg`),
          },
          {
            src: require(`@/assets/images/sTMAd10407 (1).jpg`),
          },
      ],
      categories: [
        {
          image: require(`@/assets/images/mlyL024409.svg`),
          name: 'Women\'s Clothing'
        },
        {
          image: require(`@/assets/images/HkMcw24709.svg`),
          name: 'Men\'s Clothing'
        },
        {
          image: require(`@/assets/images/PG78e24709.svg`),
          name: 'Luggage & Bags'
        },
        {
          image: require(`@/assets/images/Nr3PS24909.svg`),
          name: 'Health & Beauty, Personal Care'
        },
        {
          image: require(`@/assets/images/OiGnn24409.svg`),
          name: 'Kids & Baby'
        },
        {
          image: require(`@/assets/images/tbtaj24209.svg`),
          name: 'Food and Groceries'
        },
        {
          image: require(`@/assets/images/DaT4S24909.svg`),
          name: 'Shoes'
        },
        {
          image: require(`@/assets/images/lpvtm24409.svg`),
          name: 'Mobile Phones & Accessories'
        },
        {
          image: require(`@/assets/images/pbnEB24909.svg`),
          name: 'Cusumer Electronics'
        },
        {
          image: require(`@/assets/images/lobWx24309.svg`),
          name: 'Home & Garden'
        },
        {
          image: require(`@/assets/images/all_categories.svg`),
          name: 'All Categories'
        }
      ]
    })
}
</script>

<style scoped>
.banner{
  background: #F4F4F4;
}
</style>