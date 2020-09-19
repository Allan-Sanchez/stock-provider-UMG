<template>
  <v-container >
    <Navbar :count="0"></Navbar>

    <v-main>
      <v-row>
        <v-col cols="12">
          
          <v-card>
            <div class="d-flex flex-no-wrap justify-space-around align-center">
              <v-avatar class size="100" tile>
                <v-img :src="require('../assets/ingredients/1.jpg')"></v-img>
              </v-avatar>
              <v-card-title class="headline">Lorem ipsum dolor</v-card-title>
              <div class="d-flex align-center">
                <v-btn fab dark small color="primary">
                  <v-icon dark>mdi-minus</v-icon>
                </v-btn>
                <div class="mx-4">{{quantity}}</div>
                <v-btn fab dark small color="teal">
                  <v-icon dark>mdi-plus</v-icon>
                </v-btn>
              </div>
              <v-card-subtitle >
                 Price: $100.00
              </v-card-subtitle>
            </div>
          </v-card>
        </v-col>
        <v-col cols="12" class="d-flex justify-end align-center pr-10">
            <v-btn to="/provider-state" color="red" class="white--text" rounded>
                Total Price $ 1200.00
            </v-btn>
        </v-col>
      </v-row>
    </v-main>
  </v-container>
</template>

<script>
import Navbar from "@/components/Navbar.vue";
export default {
  name: "ProviderCart",
  components: {
    Navbar,
  },
  data() {
      return {
          quantity:1
      }
  },
};
</script>

<style >
    #app{
        background: #CBD5E0;
    }
</style>