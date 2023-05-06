<template>
<v-app-bar app color="white" class="mt-15" height="70">
     <v-toolbar color="transparent" flat>
            <v-badge color="dark" dot>
              <v-img src="./image/OIP.png" contain width="50"></v-img>
            </v-badge>
             <v-toolbar-title class="ml-1">
              <span class="blue--text">My</span><strong>Shop</strong>
            </v-toolbar-title>
    </v-toolbar>
        
       <v-spacer></v-spacer>
    
            <v-text-field label="Recherche" outlined dense v-model="search" class="v-text-field mx-2"
            prepend-inner-icon>
                <template v-slot:prepend-inner>
                    <v-icon color="black">mdi-magnify</v-icon>
                    <v-divider vertical class="ml-1"></v-divider>
                </template>
            </v-text-field>
        <v-spacer></v-spacer>

        <v-btn style="background: #f3f5f9;" large icon>
            <v-icon color="black">mdi-account-outline</v-icon>
        </v-btn>
       
        <v-btn style="background: #f3f5f9;" large icon  class="mx-1">
            <v-badge color="#3890D8" content="3">
                <v-icon color="black">mdi-cart-outline</v-icon>
            </v-badge>
        </v-btn>
    
  </v-app-bar>
</template>
<script>
export default {
    setup() {
        
    },
}
</script>
<style>
    .v-toolbar__title {
  font-size: 1rem !important;
}
.v-badge__badge {
  font-size: 10px !important;
  height: 18px !important;
  min-width: 18px !important;
  
}

.v-text-field{
    max-width:500px !important;
    max-height:55px !important;
    background: #f3f5f9 !important;
    border-radius: 20px !important;
    border: 2px solid white !important;
   
}

.bg-button-image {
  background-image: url('./image/OIP.png');
  background-size: 45px; /* pour couvrir tout le bouton avec l'image */
  background-position-x: 15px;
}
</style>


