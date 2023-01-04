<script>
import axios from "axios";

export default {
  name: "UsersView",
  components: {},

  data() {
    return {
      posts: [],
      search: "",
    };
  },

  methods: {
    /* getPosts() {
      axios
        .get("http://localhost:3000/posts")
        .then((response) => {
          console.log(response.data);
          this.posts = response.data;
        })
        .catch((error) => {
          console.log(error.message);
        });
    }, */

    /* Deletes an entry in the database */
    deleteData(id) {
      if (
        confirm(
          "Are you sure you want to delete this user from the database? This choice is permanent and cannot be regretted."
        ) == true
      ) {
        axios
          .delete(`http://localhost:3000/posts/${id}`)
          .then(this.getAllPosts())
          .catch(function (error) {
            console.log(error.response);
          });
      } else {
        return;
      }
    },

    getAllPosts() {
      axios.get("http://localhost:3000/posts").then((response) => {
        if (this.search) {
          this.posts = response.data.filter(
            (posts) =>
              posts.firstname
                .toLowerCase()
                .includes(this.search.toLowerCase()) ||
              posts.lastname
                .toLowerCase()
                .includes(this.search.toLowerCase()) ||
              posts.title.toLowerCase().includes(this.search.toLowerCase()) ||
              posts.phonenr.toLowerCase().includes(this.search.toLowerCase()) ||
              posts.company.toLowerCase().includes(this.search.toLowerCase()) ||
              posts.department
                .toLowerCase()
                .includes(this.search.toLowerCase()) ||
              posts.system.toLowerCase().includes(this.search.toLowerCase())
          );
        } else {
          console.log(response.data);
          this.posts = response.data;
        }
      });
    },
  },

  mounted() {
    console.log("Mounted");
    this.getAllPosts();
  },

  /*  {
  "id": 6,
  "firstname": "Delete",
  "lastname": "Delete",
  "title": "Delete",
  "phonenr": "123 456 789",
  "company": "Delete",
  "department": "Delete"
} */
};
</script>

<template>
  <div class="searchbar">
    <input
      type="text"
      v-model.trim="search"
      placeholder="Search for users..."
      @keyup="getAllPosts"
    />
  </div>
  <main>
    <div class="grid">
      <div v-for="post in posts" :key="post.id" class="for-class">
        <div class="user-container">
          <h1 class="user-h1">{{ post.id }}</h1>
          <h3 class="user-h3">{{ post.firstname }} {{ post.lastname }}</h3>
          <div class="user-text">Titel: {{ post.title }}</div>
          <div class="user-text">Telefonnummer: {{ post.phonenr }}</div>
          <div class="user-text">Bolag: {{ post.company }}</div>
          <div class="user-text">Avdelning: {{ post.department }}</div>
          <div class="user-text">Behörighet: {{ post.system }}</div>
          <button class="user-button" @click="deleteData(post.id)">
            Delete post
          </button>
        </div>
      </div>
    </div>

    <!-- <div class="grid">
      <div v-for="post in posts" :key="post.id" class="for-class">
      <div class="user-container">
        <h1 class="user-h1">{{ post.id }}</h1>
        <h3 class="user-h3">{{ post.firstname }} {{ post.lastname }}</h3>
        <div class="user-text">Titel: {{ post.title }}</div>
        <div class="user-text">Telefonnummer: {{ post.phonenr }}</div>
        <div class="user-text">Bolag: {{ post.company }}</div>
        <div class="user-text">Avdelning: {{ post.department }}</div>
        <button class="user-button" @click="deleteData(post.id)">
          Delete post
        </button>
      </div>
      </div>
    </div> -->
  </main>
</template>

<style scoped>
main {
  /* display: flex; */
  padding: 10px;
}

.grid {
  display: flex;
  flex-wrap: wrap;
}

.for-class {
  margin: 5px;
}

.user-container {
  display: flex;
  flex-direction: column;
  align-items: baseline;
  justify-content: space-between;
  border-style: none;
  background-color: rgba(112, 128, 144, 0.14);
  border-radius: 10px;
  padding: 10px 10px 10px 10px;
  height: auto;
  width: 270px;
}

.user-container:hover {
  background-color: hsla(160, 86%, 17%, 0.75);
  /* box-shadow: 0px 0px 3px 3px rgba(255, 255, 255, 0.4); */
  transition: 0.2s ease-out;
  transform: scale(1.1);
  z-index: 2;
}

.user-h1 {
  margin: 0px;
}

.user-h3 {
  margin: 5px;
  color: white;
}

.user-text {
  font-size: 15px;
  margin-right: 10px;
  margin: 3px 0 3px 0;
  color: white;
}

.user-button {
  margin: 5px;
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
  background-color: hsla(359, 100%, 40%, 0.47);
  transition: 0.3s ease-in-out;
}

input {
  background: #ffffff;
  border: solid #000000;
  border-radius: 6px;
  border-width: 1px;
  width: 30%;
  padding: 2px 10px;
  height: 40px;
  margin: 10px 15px 0 0px;
  position: relative;
}

.searchbar {
  display: flex;
  justify-content: center;
  padding: 10px;
}
</style>
