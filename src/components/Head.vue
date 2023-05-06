<template>
    <v-app-bar app color="#3890D8" dark flat>
        
       <v-badge color="#5F0D0" dot>
         <v-icon size="15" color="black">mdi-phone</v-icon>
       </v-badge>
       <v-toolbar-title class="mx-1" >
          <span class="black--text caption"
           onmouseover="this.style.background= '#D5F0DB';" onmouseout="this.style.background=''"
           style="border-radius: 6px;"
          >+33000000000</span>
       </v-toolbar-title>
      
       <v-badge color="#5F0D0" dot class="ml-1">
         <v-icon size="15" color="black">mdi-message</v-icon>
       </v-badge>
       <v-toolbar-title class="ml-1" >
          <span class="black--text caption"
           onmouseover="this.style.background= '#D5F0DB';" onmouseout="this.style.background=''"
           style="border-radius: 6px;"
          >gmail@gmail.com</span>
       </v-toolbar-title>
       <v-spacer></v-spacer>

       <v-divider vertical class=""></v-divider>
        
       <span class="black--text caption mx-2"
                 style="border-radius: 6px;"
                 onmouseover="this.style.background= '#D5F0DB';" onmouseout="this.style.background=''"
                 >Theme FAQ's</span> 
    
       <span class="black--text caption mx-2"
                 style="border-radius: 6px;"
                 onmouseover="this.style.background='#D5F0DB';" onmouseout="this.style.background=''"
                 >Besoin d'aide</span> 
      
        <v-icon size="15"  color="black">mdi-flag</v-icon>
        <span class="black--text caption"
                 style="border-radius: 6px;"
                 onmouseover="this.style.background='#D5F0DB';" onmouseout="this.style.background=''"
                 >FR</span> 
       
       <v-icon class="ml-2" size="15" color="black">mdi-flag</v-icon>
       <span class="black--text caption"
                 style="border-radius: 6px;"
                 onmouseover="this.style.background='#D5F0DB';" onmouseout="this.style.background=''"
                 >USD</span> 

  </v-app-bar>
</template>

<script>
export default {
  name: "HeadItem",
};
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
</style>



















