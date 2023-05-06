<template>
  <v-item-group mandatory class="mt-n1">
    <v-container>
      <v-row justify="center" class="space">
        <v-col
          cols="12"
          xs="12"
          sm="4"
          md="2"
          v-for="(cetegory, i) in categories"
          :key="i"
        >
          <v-item v-slot="{ active, toggle }">
            <v-card
              :color="active ? '#f3f5f9' : 'white'"
              :class="active ? 'borderme' : 'borderout'"
              class="d-flex align-center rounded-lg mx-2"
              dark
              height="180"
              @click="toggle"
              flat
            >
              <v-row>
                <v-col cols="12" sm="12">
                  <v-list-item three-line class="text-center">
                    <v-list-item-content>
                      <div align="center" justify="center">
                        <v-img
                          :src="cetegory.img"
                          max-height="80"
                          max-width="80"
                          contain
                        ></v-img>
                      </div>
                      <v-list-item-subtitle
                        :class="active ? 'blue--text' : 'black--text'"
                        class="caption mt-4"
                        >{{ cetegory.title }}</v-list-item-subtitle
                      >
                    </v-list-item-content>
                  </v-list-item>
                </v-col>
              </v-row>
            </v-card>
          </v-item>
        </v-col>
      </v-row>
    </v-container>
  </v-item-group>
</template>

<script>
export default {
    name: "CategorieItem",
  data: () => ({
    categories: [
      { img: "https://fakestoreapi.com/img/71YXzeOuslL._AC_UY879_.jpg", title: "Mens Casual Slim Fit" },
      { img: "https://fakestoreapi.com/img/61sbMiUnoGL._AC_UL640_QL65_ML3_.jpg", title: "Solid Gold Petite Micropave" },
      { img: "https://fakestoreapi.com/img/61IBBVJvSDL._AC_SY879_.jpg", title: "WD 2TB Elements Portable External Hard Drive - USB 3.0" },
      { img: "https://fakestoreapi.com/img/81QpkIctqPL._AC_SX679_.jpg", title: "Acer SB220Q bi 21.5 inches Full HD (1920 x 1080) IPS Ultra-Thin" },
      { img: "https://fakestoreapi.com/img/71HblAHs5xL._AC_UY879_-2.jpg", title: "Rain Jacket Women Windbreaker Striped Climbing Raincoats" },
      { img: "https://fakestoreapi.com/img/61pHAEJ4NML._AC_UX679_.jpg", title: "DANVOUY Womens T Shirt Casual Cotton Short" },
    ],
  }),
};
</script>

<style>
</style>