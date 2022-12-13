<template>
  <main>

    <div class="container">

      <div class="border">
        <h1> Your total is: {{ totalPrice }} SEK</h1>
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
          <button @click="add">Add to cart</button>
        </div>
      </div>
    </div>




  </main>
</template>

<script>
export default {
  name: "Homeview",
  totalPrice: 0,
    data() {
      return {
        totalPrice: 0,
        items: [
          {
            id: "1",
            title: "Name",
            price: "600",
          },
          {
            id: "2",
            title: "Name 2",
            price: "1000",
          },
          {
            id: "3",
            title: "Name 3",
            price: "10",
          },
          {
            id: "4",
            title: "Name 4",
            price: "650",
          },
          {
            id: "5",
            title: "Name 5",
            price: "1500",
          },
          {
            id: "6",
            title: "Name 6",
            price: "50",
          }
        ]
      }
    },
    
    methods: {
      add() {
        this.items.price = totalPrice;
        console.log(totalPrice);

      /* this.items.price.push(this.item.totalArray); */
      /* console.log(totalArray); */
      }
    },

    computed: {
      total() {
        return console.log(totalArray);
      }
    }
}
</script>

<script setup>
import { computed } from '@vue/reactivity';
import { ref } from 'vue';

const numberOne = ref(0);
const numberTwo = ref(0);

</script>

<style scoped>

main {
  display: flex;
  margin-top: 20px;
  padding: 10px;
}

.grid {
  display: flex;
  flex-wrap: wrap
}

.for-class {
  margin: 5px;
}

.container {

  margin: 5px;

  padding: 15px;
  align-items: center;
  display: flex;
  justify-content: center;
  flex-direction: column;
  border-style: none;
  background-color: rgba(112, 128, 144, 0.14);
  border-radius: 10px;
  width: 300px;
  height: 300px;
}

.border {
  align-items: center;
  display: flex;
  justify-content: center;
  border-radius: 10px;
  border: solid 0.5px grey;
  width: 200px;
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
  background-color: rgba(158, 171, 184, 0.600);
  transition: 0.3s ease-in-out;
}

.card-container {
  display: flex;
  justify-content: center;
  flex-direction: column;
  border-style: none;
  background-color: rgba(112, 128, 144, 0.14);
  border-radius: 10px;
  padding: 15px;
  height: 130px;
  width: 200px;
}

.card-title {
  font-size: 15px;
  margin-right: 10px;
}

.card-container:hover {
    background-color: hsla(160, 100%, 37%, 0.2);
}


</style>