<template>
  <v-footer dark padless class="mt-15">
    <v-card flat tile class="black white--text py-12 px-5" width="100%">
      <v-row>
        <v-col cols="12" xs="12" sm="6" md="4" class="pa-16">
          <v-toolbar color="transparent" flat>
            <v-badge color="dark" dot>
              <v-img src="./image/OIP.png" contain width="50"></v-img>
            </v-badge>
             <v-toolbar-title class="ml-1">
              <span class="blue--text">My</span><strong>Shop</strong>
            </v-toolbar-title>
          </v-toolbar>
          <v-card-text class="pt-0">
              <v-btn style="background: #f3f5f9;" class="mx-1" large icon v-for="icon in icons" :key="icon">
                 <v-icon color="black">{{icon}}</v-icon>
            </v-btn>
          </v-card-text>
        </v-col>
        <v-col cols="12" xs="12" sm="6" md="2">
          <v-card-text class="white--text pt-0">
            <h3>A propos</h3>
          </v-card-text>
          <v-card-text class="grey--text">Comment ça marche</v-card-text>
          <v-card-text class="grey--text mt-n4"> Nos Programmes </v-card-text>
          <v-card-text class="grey--text mt-n4"> Promotions </v-card-text>
          <v-card-text class="grey--text mt-n4"> Parrainer un ami </v-card-text>
        </v-col>
        <v-col cols="12" xs="12" sm="6" md="2">
          <v-card-text class="white--text pt-0">
            <h3>Livraison</h3>
          </v-card-text>
          <v-card-text class="grey--text"> Coût de la livraison </v-card-text>
          <v-card-text class="grey--text mt-n4"> Méthode de paiement </v-card-text>
          <v-card-text class="grey--text mt-n4"> Astuce de livraison </v-card-text>
          <v-card-text class="grey--text mt-n4"> Retours </v-card-text>
        </v-col>
        <v-col cols="12" xs="12" sm="6" md="4">
          <v-card-text class="white--text pt-0">
            <h3>Contact</h3>
          </v-card-text>
          <v-card-text class="grey--text"> AAE MyShop </v-card-text>
          <v-card-text class="grey--text mt-n4">25 rue de la Jack</v-card-text>
          <v-card-text class="grey--text mt-n4"> www.MyShop.com </v-card-text>
          <v-card-text class="grey--text mt-n4"> -B8254552214 </v-card-text>
        </v-col>
        <v-col cols="12" xs="12" sm="6" md="4">
          <v-card-text class="white--text pt-0">
            <h3>Partenaires</h3>
          </v-card-text>
          <v-card-text class="grey--text"> PawnShop </v-card-text>
          <v-card-text class="grey--text mt-n4">ESS</v-card-text>
          <v-card-text class="grey--text mt-n4"> Nike </v-card-text>
        </v-col>
      </v-row>
    </v-card>
  </v-footer>
</template>

<script>
export default {
  name: "FooterItem",
  data: () => ({
    icons: [
      "mdi-facebook",
      "mdi-gmail",
      "mdi-twitter",
      "mdi-linkedin",
    ],
  }),
};
</script>

<style>
</style>