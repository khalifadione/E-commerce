<template>
  <v-container fluid>
    <v-card
      color="#3853D8"
      height="120px"
      tile
      flat
      class="d-flex align-center justify-center"
      dark
    >
      <v-row>
        <v-col cols="12" sm="12">
          <h4 class="text-center">MEN'S LIFESTYLE SHOES</h4>
        </v-col>
        <v-col cols="12" sm="12">
          
        </v-col>
      </v-row>
    </v-card>
    <v-card tile class="mx-16 mt-n10 card1" color="white">
      <v-row>
        <v-col cols="12" sm="8" class="pr-0">
          <v-card height="400px" tile flat color="#3890D8">
            <v-row>
              <v-col cols="12" sm="4" class="pl-8 pt-5">
                <v-btn color="black" dark class="withoutupercase" small tile>
                  new
                </v-btn>
                <h6 class="white--text mt-8">MOUNTAIN BIKE</h6>
                <h3 class="white--text mt-5">Trek Speed Concept</h3>
                <v-btn
                  rounded
                  color="#4C9CDB"
                  dark
                  class="withoutupercase px-8 mt-10"
                >
                  More Info
                </v-btn>
              </v-col>
              <v-col cols="12" sm="8">
                <v-carousel hide-delimiters hide-controls>
                <v-carousel  cycle :interval="2000">
                  <v-carousel-item v-for="(item, i) in items" :key="i" :src="item.src"  max-height="400"
                  max-width="400"
                  contain
                  class="mt-n2">
                  </v-carousel-item>
                </v-carousel>
                </v-carousel>
              </v-col>
            </v-row>
          </v-card>
        </v-col>
        <v-col cols="12" sm="4" class="pl-0">
          <v-card height="250px" tile flat color="#6857E1">
            <v-row>
              <v-col cols="12" sm="6" class="pl-8 pt-5">
                <v-btn color="black" dark class="withoutupercase" small tile>
                  new
                </v-btn>
                <h6 class="white--text mt-8">DOWN JACKET</h6>
                <h3 class="white--text mt-5">Sale Collection 2015</h3>
                <v-btn
                  rounded
                  color="#8375E7"
                  dark
                  class="withoutupercase px-8 mt-3"
                >
                  More Info
                </v-btn>
              </v-col>
              <v-col cols="12" sm="6">
                <v-img
                  src="https://fakestoreapi.com/img/71YXzeOuslL._AC_UY879_.jpg"
                  max-height="400"
                  max-width="420"
                  contain
                  class="mt-n2"
                ></v-img>
              </v-col>
            </v-row>
          </v-card>
        </v-col>
      </v-row>
     
    </v-card>
  </v-container>
</template>

<script>

  export default {
   
  name: 'DashboardItem',
    data: () => ({
          loading: false,
          postslist: [],
          items: [
          {
            src: 'https://fakestoreapi.com/img/81fPKd-2AYL._AC_SL1500_.jpg',
          },
          {
            src: 'https://fakestoreapi.com/img/71-3HjGNDUL._AC_SY879._SX._UX._SY._UY_.jpg',
          },
          { 
            src: 'https://fakestoreapi.com/img/71li-ujtlUL._AC_UX679_.jpg',
          },
          { 
            src: 'https://fakestoreapi.com/img/71YXzeOuslL._AC_UY879_.jpg',
          },
          { 
            src: 'https://fakestoreapi.com/img/71pWzhdJNwL._AC_UL640_QL65_ML3_.jpg',
          },
        ],
     }),
    mounted: async function(){
        this.loading= true;
        const response = await  fetch('https://fakestoreapi.com/products');
        this.postslist = await response.json();
        console.log(this.postslist);
        this.loading=false;

    }

  }
</script>

<style>
.container {
  padding: 0px !important;
}
.v-btn.withoutupercase {
  text-decoration: none;
}
.v-chip.v-size--default {
  border-radius: 50px !important;
  font-size: 14px !important;
  height: 40px !important;
  width: 40px !important;
}
.v-card--reveal {
  align-items: center;
  bottom: 0;
  justify-content: center;
  opacity: 0.5;
  position: absolute;
  width: 100%;
}
.card1 {
  z-index: 2;
}
.card2 {
  z-index: 1;
}
.v-btn--icon.v-size--small .v-icon, 
.v-carousel__controls,.v-btn--icon.v-size--default .v-icon
{ display: none !important;}

</style>