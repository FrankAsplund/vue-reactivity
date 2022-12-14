<template>
  <main>
    <div class="container">
      <div class="border">
        <h1>Your total is: {{ totalPrice }} SEK</h1>
      </div>

      <!-- <button @click="numberOne++">Increase 1st number</button>
      <h1>{{ numberOne }}</h1>

      
      <button @click="numberTwo++">Increase 2nd number</button>
      <h1>{{ numberTwo }}</h1>
      
      <div class="border">
        <h1>{{ numberOne }} + {{ numberTwo }} = {{ numberOne + numberTwo }}</h1>
      </div> -->
    </div>

    <div class="grid">
      <div v-for="item in items" :key="item.id" class="for-class">
        <div class="card-container">
          <h1 class="card-h1">{{ item.id }}</h1>
          <div class="card-title">{{ item.title }}</div>
          <div class="card-text">{{ item.price }}</div>
          <button class="card-button" @click="add(item)">Add to cart</button>
        </div>
      </div>
    </div>
  </main>
</template>

<script>
export default {
  name: "Homeview",
  data() {
    return {
      totalPrice: 0,
      items: [
        {
          id: "1",
          title: "Name",
          price: 600,
        },
        {
          id: "2",
          title: "Name 2",
          price: 1000,
        },
        {
          id: "3",
          title: "Name 3",
          price: 10,
        },
        {
          id: "4",
          title: "Name 4",
          price: 650,
        },
        {
          id: "5",
          title: "Name 5",
          price: 1500,
        },
        {
          id: "6",
          title: "Name 6",
          price: 50,
        },
      ],
    };
  },

  methods: {
    add(item) {
      /* var totalPrice = 0; */
      console.log(item.price);
      this.totalPrice += item.price;
      console.log("Total price is: ", this.totalPrice);
      return this.totalPrice;
    },
  },

  computed: {
    total() {
      return console.log(totalArray);
    },
  },
};
</script>

<script setup>
import { computed } from "@vue/reactivity";
import { ref } from "vue";

const numberOne = ref(0);
const numberTwo = ref(0);
/* const totalPrice = ref(0); */

/* computed: {},

methods: {
    add(item) {
      console.log(item.price);
      totalPrice = item.price;
      console.log("Total price is: ", totalPrice);
      return totalPrice;
    },
  }, */
</script>

<style scoped>
main {
  display: flex;
  margin-top: 20px;
  padding: 10px;
}

.grid {
  display: flex;
  flex-wrap: wrap;
}

.for-class {
  margin: 5px;
}

.container {
  margin: 5px 10px 0 0;

  padding: 15px;
  align-items: center;
  display: flex;
  justify-content: center;
  flex-direction: column;
  border-style: none;
  background-color: rgba(112, 128, 144, 0.14);
  border-radius: 10px;
  width: 300px;
  height: 330px;
}

.border {
  align-items: center;
  display: flex;
  justify-content: center;
  border-radius: 10px;
  border: solid 0.5px grey;
  width: 200px;
  padding: 10px;
}

button {
  cursor: pointer;
  justify-content: center;
  border-radius: 10px;
  border: solid 0.5px grey;
  color: white;
  background-color: rgba(112, 128, 144, 0.14);
  width: 150px;
  height: 50px;
}

button:hover {
  color: black;
  background-color: rgba(158, 171, 184, 0.6);
  transition: 0.3s ease-in-out;
}

.card-container {
  display: flex;
  justify-content: center;
  flex-direction: column;
  border-style: none;
  background-color: rgba(112, 128, 144, 0.14);
  border-radius: 10px;
  padding: 5px 10px 5px 10px;
  height: 170px;
  width: 250px;
}

.card-title {
  font-size: 15px;
  margin-right: 10px;
}

.card-container:hover {
  background-color: hsla(160, 100%, 37%, 0.2);
}

.card-h1 {
  margin: 0px;
}

.card-text {
  margin: 3px 0 3px 0;
}

.card-button {
  margin: 5px;
}
</style>
