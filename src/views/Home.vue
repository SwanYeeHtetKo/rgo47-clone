<template>
  <div class="home">
    <Banner/>

    <div class="data">

      <!-- DealOfTheDay -->
      <div>
        <DealOfTheDay/>
      </div>
      
      <!-- Covid19 -->
      <div>
        <Covid19/>
      </div>
      
      <!-- ads -->
      <div>
        <v-container>
          <v-img src="@/assets/images/1Mu9s03504.webp"/>
        </v-container>
      </div>

      <!-- Available Brands -->
      <div>
        <AvailableBrands/>
      </div>

    </div>

    <!-- Categories -->
    <div class="categories">
      <Categories/>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import Banner from '@/components/Banner'
import DealOfTheDay from '@/components/DealOfTheDay'
import Covid19 from '@/components/Covid19'
import AvailableBrands from '@/components/AvailableBrands'
import Categories from '@/components/Categories'
export default {
  name: 'Home',
  components: {
    Banner,
    DealOfTheDay,
    Covid19,
    AvailableBrands,
    Categories
  },
  data: () => ({
      
    }),
}
</script>

<style scoped>
.data {
  background: #fff;
}

.categories{
  background: #F4F4F4;
}

</style>