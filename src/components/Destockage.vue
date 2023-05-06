
<template>
  <v-row justify="center" class="space px-16 pb-5">
    <v-col cols="12" xs="12" sm="6" md="4" v-for="(pack, i) in packs" :key="i">
      <v-card class="mx-auto" max-width="300" color="" flat outlined>
         <v-btn dark class="withoutupercase" small tile style="
                         background: red; transform: skew(0, -5deg); height: 30px">
                          Déstockage -75%
        </v-btn>
        <div align="center" justify="center">
          <v-img
            class="mt-1"
            max-height="300"
            max-width="300"
            contain
            :src="pack.img"
          ></v-img>
        </div>

        <v-card-title class="">{{ pack.title }}</v-card-title>
        <v-card-title class="grey--text text-grey-darken-1 caption mt-n6">{{
          pack.subtitle
        }}</v-card-title>
        <v-card-title class="mt-n4">{{ pack.price }}</v-card-title>

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
    name: "DestockageItem",
  data: () => ({
      bpm: 1,
    packs: [
      { img: "https://fakestoreapi.com/img/81fPKd-2AYL._AC_SL1500_.jpg", price: "55€" },
      { img: "https://fakestoreapi.com/img/71li-ujtlUL._AC_UX679_.jpg", price: "55€" },
      { img: "https://fakestoreapi.com/img/71YXzeOuslL._AC_UY879_.jpg",  price: "55€" },
     
    ],
  }),
   methods: {
      decrement () {
        this.bpm--
      },
      increment () {
        this.bpm++
      },
     
    },
};
</script>

<style>
</style>