<template>
  <v-container>
    <Navbar></Navbar>
    <v-main>
      <v-row>
        <v-col v-for="(item, index) in products" :key="index" cols="4">
          <v-card class="mx-auto my-12" max-width="374">
            <v-img height="200" :src="require(`../assets/ingredients/${item.image}`)"></v-img>

            <v-card-title>{{item.name}}</v-card-title>

            <v-card-text>
              <v-row align="center" class="mx-0">
                <v-rating
                  :value="item.rating"
                  color="amber"
                  dense
                  half-increments
                  readonly
                  size="14"
                ></v-rating>

                <div class="grey--text ml-4">{{item.rating}} ({{item.value}})</div>
              </v-row>

              <div class="my-4 subtitle-1">Price $ {{item.price}}</div>

              <div>{{item.description}}</div>
            </v-card-text>

            <v-card-actions class="d-flex justify-end">
              <v-btn color="red lighten-2" class="white--text" @click="addCart(item.id)">Add Cart</v-btn>
            </v-card-actions>
          </v-card>
        </v-col>
      </v-row>
    </v-main>
  </v-container>
</template>

<script>
import Navbar from "@/components/Navbar.vue";
export default {
  name: "ProviderHome",
  components: {
    Navbar,
  },
  data() {
    return {
      products: [
        {
          id: 1,
          name: "Flour Bag",
          image: "1.jpg",
          value: Math.floor(Math.random() * 400),
          rating: 3,
          price: 400,
          description:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit. Cupiditate, eos!",
        },
        {
          id: 2,
          name: "Salt Bag",
          image: "2.jpg",
          value: Math.floor(Math.random() * 400),
          rating: 4,
          price: 100,
          description:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit. Cupiditate, eos!",
        },
        {
          id: 3,
          name: "Milk",
          image: "3.jpg",
          value: Math.floor(Math.random() * 400),
          rating: 3.5,
          price: 600,
          description:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit. Cupiditate, eos!",
        },
        {
          id: 8,
          name: "Eggs",
          image: "8.png",
          value: Math.floor(Math.random() * 400),
          rating: 4,
          price: 100,
          description:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit. Cupiditate, eos!",
        },
      ],
    };
  },
  methods: {
    addCart(item) {
      console.log(item);
    },
  },
};
</script>