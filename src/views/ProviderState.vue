<template>
  <v-container>
    <v-main>
      <v-row justify="center">
        <v-col cols="6" class="mt-15">
          <h3
            class="text-h3 text-center blue-grey--text text--darken-1 font-weight-bold"
          >Follow your Order</h3>
          <v-form class="d-flex align-center mt-5">
            <v-text-field
              v-model="name"
              :counter="10"
              :rules="nameRules"
              label="Type your purchase code"
              required
            ></v-text-field>
            <v-btn color="primary" rounded class="ml-6">Search</v-btn>
          </v-form>
        </v-col>
      </v-row>
      <v-row justify="center">
        <v-col cols="3">
          <v-card>
            <v-card-title class="d-flex justify-center">Bill</v-card-title>
            <v-card-text>No.#154645656654 Pedido ya entregado el pedido se realizo bajo la fecha 20/09/20 20:50.</v-card-text>
            <v-card-actions class="d-flex justify-center">
              <v-chip class="ma-2"  color="teal" text-color="white" >
                <v-avatar left>
                  <v-icon>mdi-checkbox-marked-circle</v-icon>
                </v-avatar>Order delivered
              </v-chip>
            </v-card-actions>
          </v-card>
          
        </v-col>
      </v-row>
    </v-main>
  </v-container>
</template>

<script>
export default {
  name: "ProviderState",
};
</script>

<style >
#app {
  background: #cbd5e0;
}
</style>