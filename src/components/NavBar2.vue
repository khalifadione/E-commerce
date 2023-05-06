<template>
  <v-app-bar app flat class="v-app-bar3" height="50">
    
       

     <v-menu style="margin-top: 20px;" >
        <template v-slot:activator="{ on, attrs }">
          <v-btn icon large v-bind="attrs" v-on="on" >
            <v-icon color="black">mdi-menu</v-icon> 
          </v-btn>
          <span class="black--text caption">Menu</span>
        </template>
        <v-list>
           <v-list-item v-for="(n, index) in optionIcone" :key="index"  @click="() => {}">
              <v-list-item-icon>
                   <v-icon class="mx-2" dark color="black">{{n}}</v-icon>
                   <span>{{propriete[index]}}</span>
              </v-list-item-icon>
          </v-list-item>
        </v-list>
      </v-menu>


       
       <v-spacer></v-spacer>
        <span v-for="n in optionAppBar3" :key="n" class="black--text caption mx-2 " style="border-radius: 6px;"
                 onmouseover="this.style.background='#D5F0DB';" onmouseout="this.style.background=''"
                >{{n}}</span> 
         
         
      
  </v-app-bar>
</template>

<script>
 export default {
  props: {
  },
    name: "HeadItem",
     data: () => ({
          optionIcone: ["mdi-human-male", "mdi-human-female", "mdi-shoe-print", 
          "mdi-briefcase", "mdi-tshirt-crew", "mdi-desktop-tower"],
          propriete: ["Homme","Femme", "Chaussures", "Accessoire","Habits", "Electronique"],
          optionAppBar3: ["Accueil","Pages","Mon Compte","Contact"]
     }),

  }
</script>

<style>



  
.v-app-bar3{
   margin-top: 130px !important; 
}
</style>