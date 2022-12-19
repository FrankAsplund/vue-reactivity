<script>
import axios from "axios";

export default {
  name: "AboutView",
  data() {
    return {
      formData: {
        firstname: "",
        lastname: "",
        title: "",
        phonenr: "",
        company: "",
        department: ""
      },
    };
  },
  methods: {
    createUser() {
      if(!confirm('Are you sure?')) {
        e.preventDefault();
    }
      axios
        .post("http://localhost:3000/posts", this.formData)
        .then((response) => console.log(response))
        .catch((error) => console.log(error));
    },
  },
};
</script>

<template>
  <main>
      <div class="frame-4">
        <h1 class="text">Skapa användarkonto</h1>

        <div class="subText">
          Här kan du skapa ett nytt användarkonto i AD. Vänligen fyll i
          uppgifterna nedan.
        </div>
        <div class="frame-5">
          <form @submit.prevent="createUser">
          <div class="header">Ny användare</div>

          <div class="grid">

            <div class="form-class">
              <label for="firstname" class="label-short">Förnamn
                <span class="required-label"> *</span>
              </label>
              <input name="firstname" class="input-short" type="text" v-model="formData.firstname" required>
            </div>

              <div class="form-class">
                <label for="lastname" class="label-short">Efternamn
                <span class="required-label"> *</span>
              </label>
              <input name="lastname" class="input-short" type="text" v-model="formData.lastname" required>
              </div>

              <br>
          </div>

          <div class="grid">
          <div class="form-class">
            <label for="title">Titel
              <span class="required-label"> *</span>
            </label>
            <br>
            <input name="title" type="text" v-model="formData.title" required>
          </div>


          <div class="form-class">
            <label for="phonenr">Telefonnummer
              <span class="required-label"> *</span>
            </label>
            <br>
            <input name="phonenr" type="text" v-model="formData.phonenr" required>
          </div>


          <div class="form-class">
            <label for="company">Bolag
              <span class="required-label"> *</span>
            </label>
            <br>
            <input name="company" type="text" v-model="formData.company" required>
          </div>


          <div class="form-class">
            <label for="department">Avdelning
              <span class="required-label"> *</span>
            </label>
            <br>
            <input name="department" type="text" v-model="formData.department" required>
          </div>
                      
        </div>

          <button class="skicka"> Skicka </button>


          </form>
        </div>
      </div>
    
  </main>
</template>

<style>
main {
  display: flex;
  justify-content: center;
}

.frame-1,
.frame-1 * {
  box-sizing: border-box;
}

.frame-1 {
  display: flex;
  justify-content: center;
  background: #ffffff;
  width: 100%;
  height: 1553px;
  position: relative;
}
.frame-4 {
  background-color: hsla(160, 100%, 37%, 0.05);
  width: 100%;
  border: solid #000000;
  
  border-width: 1px;
  height: auto;
  display: flex;
  justify-content: center;
  flex-direction: column;
  align-items: center;
  position: relative;
}
.text {
  color: #ffffff;
  text-align: left;
  font: 600 40px "Inter", sans-serif;
  position: relative;
  display: flex;
  justify-content: center;
  width: 475px;
}
.subText {
  color: #ffffff;
  text-align: left;
  font: 400 20px "Inter", sans-serif;
  position: relative;
  display: flex;
  justify-content: center;
  width: 797px;
  margin: 0 0 15px 0;
}

.grid {
  margin: 20px 0 20px 0;
  padding: 10px;
  display: grid;
  border: solid #00000063;
  border-radius: 6px;
  border-width: 0.3px;
}

.frame-5 {
  background: #fff;
  border-radius: 5px;
  min-width: 600px;
  height: auto;
  position: relative;
  padding: 15px 25px 25px 25px;
  box-shadow: 0px 4px 4px 0px rgba(255, 255, 255, 0.7);
  margin: 0 0 3rem 0;
}
.header {
  color: #000000;
  text-align: left;
  font: 600 20px "Inter", sans-serif;
  position: relative;
  width: 168px;
}

label {
  color: #000000;
  font: 20px "Inter", sans-serif;
  font-weight: 500;
  line-height: 1;
  margin-bottom: 10px;
  padding: 10px;
}

.required-label {
    color: #CD2036;
}

input {
  background: #ffffff;
  border: solid #000000;
  border-radius: 6px;
  border-width: 1px;
  width: 70%;
  padding: 2px 10px;
  height: 40px;
  margin: 10px 15px 0 0px;
  position: relative;
}

.input-short {
  width: 30%;
}

.form-class {
  margin: 10px 0 15px 0;
}

.skicka {
  background-color: #fff;
  border-radius: 6px;
  color: black;
  font: 400 16px "Inter", sans-serif;
  width: 120px;
  height: 50px;
}

.skicka:hover {
  transition: 0.5s ease-in-out;
  background-color: hsla(161, 68%, 15%, 0.628);
  color: #fff;
}

</style>
