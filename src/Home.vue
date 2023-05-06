<template>
  <v-app>
    
    <v-main>
  
     
      <Head class="index" />
      <NavBar1 />
      <NavBar2 />
      <v-container>
        <v-row>
          <v-col cols="12">
            <v-card class="mx-auto rounded-xl"  color="white">
              <v-card-title class="top ml-10 white--text">
                <h2 class="title1" ></h2>
              </v-card-title>
              <v-row>
                <v-col cols="12" sm="8" class="pr-0">
                  <v-card height="400px" tile flat color="white" class="ml-3 mx-10">
                    <v-row>
                      <v-col cols="12" sm="4" class="pl-8 pt-5">
                        <v-btn dark class="withoutupercase" small tile style="
                         background: red; transform: skew(0, -10deg); height: 50px">
                          Promotion
                        </v-btn>
                        <h4 class="black--text mt-8">Réduction</h4>
                        <h1 class="black--text mt-5">50% pour votre premier achat</h1>
                        <v-btn
                          rounded
                          color="#3890D8"
                          dark
                          class="withoutupercase px-8 mt-10"
                        >
                          Plus Info
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
                  <v-card height="250px" tile flat color="#3890D8" class="mx-3 rounded-xl">
                    <v-row>
                      <v-col cols="12" sm="6" class="pl-8 pt-5">
                        <v-btn color="black" dark class="withoutupercase" small tile>
                          Nouveauté
                        </v-btn>
                        <h5 class="white--text mt-8">JACKET Homme</h5>
                        <h2 class="white--text mt-5">Vente en Collection</h2>
                        <v-btn
                          rounded
                          color="#3890D8"
                          dark
                          class="withoutupercase px-8 mt-3"
                        >
                          Plus Info
                        </v-btn>
                      </v-col>
                      <v-col cols="12" sm="6">
                        <v-img
                          src="./components/image/blouson-cuir-homme.png"
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
          </v-col>
        
          <v-toolbar flat color="transparent">
            <v-toolbar-title class="text-h6 white--text" style="
              background: black; " >Flash Vente</v-toolbar-title>
            <v-spacer></v-spacer>
            <v-btn-toggle v-model="toggle_exclusive" group color="blue">
              <v-btn>
                <v-icon>mdi-chevron-left</v-icon>
              </v-btn>
              <v-btn>
                <v-icon>mdi-chevron-right</v-icon>
              </v-btn>
            </v-btn-toggle>
          </v-toolbar>

            
          
        </v-row>
      </v-container>

      <FlashVente />
      <v-toolbar flat color="transparent" class="mt-5">
          <v-toolbar-title class="text-h6">Nouvelle Collection</v-toolbar-title>
          <v-spacer></v-spacer>
          <v-btn rounded color="#3890D8" dark class="px-8">Voir tout</v-btn>
      </v-toolbar>
      <Produits />
      <v-card flat color="#E2F2E5" class="rounded-lg mt-8">
            <v-toolbar flat color="transparent" class="mb-4">
              <v-toolbar-title class="text-h6 mt-5"
                >Déstockage</v-toolbar-title
              >
              <v-spacer></v-spacer>
            </v-toolbar>
       </v-card>
      <Destockage />
           <v-card
            flat
            color="#E2F2E5"
            class="rounded-xl mtop mbottom mx-10 pa-4 mt-10"
            height="350"
          >
            <v-row>
              <v-col cols="12" xs="12" sm="6" md="7">
                <h1 class="mt-16">Télécharger l'application</h1>
                <p>
                  Application disponible en version android et apple<br />
                
                </p>
                <v-btn color="black" dark class="mb-10">
                  <v-icon color="white" left>fab fa-apple</v-icon>
                  App Store
                </v-btn>
                <v-btn color="black" dark class="ml-4 mb-10">
                  <v-icon color="white" left>fab fa-google-play</v-icon>
                  Play Store
                </v-btn>
              </v-col>
              <v-col cols="12" xs="12" sm="12" md="5">
                 <v-card
                  class="rounded-xl mt-n16 ml-16 mobile"
                  outlined
                  flat
                  height="450"
                  width="200"
                >
                  <v-img src="./components/image/telVersion.png" >
                       
                  </v-img>
                </v-card>
              </v-col>
            </v-row>
          </v-card>
    </v-main>
      <Footer />
  </v-app>
</template>

<script>

import NavBar1 from './components/NavBar1';
import NavBar2 from './components/NavBar2';
import Head from './components/Head';
import FlashVente from './components/FlashVente.vue';
import Produits from './components/Produits.vue';
import Destockage from './components/Destockage.vue';
import Footer from './components/Footer.vue';





export default {
  methods: {
  },
  name: 'HomeItem',

  components: {
    
    Head,
    NavBar1,
    NavBar2,
    FlashVente,
    Produits,
    Destockage,
    Footer
    
    
  },

  data: () => ({

     items: [
          {
            src: 'https://fakestoreapi.com/img/81fPKd-2AYL._AC_SL1500_.jpg',
          },
          {
            src: 'https://fakestoreapi.com/img/81QpkIctqPL._AC_SX679_.jpg',
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
          {
            src: 'https://fakestoreapi.com/img/61pHAEJ4NML._AC_UX679_.jpg',
          },
          {
            src: 'https://fakestoreapi.com/img/71z3kpMAYsL._AC_UY879_.jpg',
          },
        ],
    //
  }),
};
</script>

<style>
 .indexe{
   z-index: 9999;
 }
 .v-btn--icon.v-size--small .v-icon, 
.v-carousel__controls,.v-btn--icon.v-size--default
{ display: none !important;}

</style>
