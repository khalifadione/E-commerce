<template>
  <v-row justify="center" class="space px-16">
    <v-col
      cols="12"
      xs="12"
      sm="6"
      md="4"
      v-for="(product, i) in postslist"
      :key="i"
    >
      <v-card class="mx-auto rounded-lg" max-width="300" color="" flat outlined>
        <div align="center" justify="center">
          <v-img
            max-height="300"
            max-width="300"
            contain
            :src="product.image"
          ></v-img>
        </div>

        <v-card-title class="">{{ product.title }}</v-card-title>
        <v-card-title class="grey--text text-grey-darken-1 caption mt-n6">{{
          product.subtitle
        }}</v-card-title>
        <v-card-title class="mt-n4">{{ product.price }}€</v-card-title>

        <v-card-actions class="mx-2 mt-n4">
          <v-btn outlined class="mt-n2 add">
            <v-icon color="#3890D8" @click="decrement"> mdi-minus </v-icon>
          </v-btn>

          <strong class="mx-2" v-text="bpm"></strong>
          <v-btn outlined class="mt-n2 add">
            <v-icon color="#3890D8" @click="increment"> mdi-plus </v-icon>
          </v-btn>
          <v-spacer></v-spacer>
          <v-btn class="mx-2 mt-n3" fab dark small color="#3890D8">
            <v-icon dark> mdi-shopping </v-icon>
          </v-btn>
        </v-card-actions>
      </v-card>
    </v-col>
  </v-row>
</template>

<script>
export default {
    name: "ProductsItems",
  data: () => ({
          nbrProduits: 1,
          loading: false,
          postslist: [],
         
     }),
    mounted: async function(){
        this.loading= true;
        const response = await  fetch('https://fakestoreapi.com/products');
        this.postslist = await response.json();
        console.log(this.postslist);
        this.loading=false;


    },
     methods: {
      decrement () {
        this.nbrProduits--
      },
      increment () {
        this.nbrProduits++
      },
     
    },
};
</script>

<style>
</style>