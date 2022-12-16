<script setup>
import { RouterLink, RouterView } from "vue-router";
</script>

<template>
  <nav>
    <div class="navbar">
      <img
        alt="logo"
        class="logo"
        src="@/assets/logo.svg"
        width="120"
        height="120"
      />
      <h1>Vue Sean assignment</h1>
      <div class="router">
        <RouterLink to="/">Home</RouterLink>
        <RouterLink to="/about">About</RouterLink>
      </div>
    </div>
  </nav>
</template>

<style scoped>
h1 {
  margin-right: 1rem;
}
.router {
  margin-left: 3rem;
}
.logo {
  margin-right: 1rem;
  padding: 20px;
}
nav {
  align-items: center;
  /* width: 100vw; */
  font-size: 15px;
}
.navbar {
  align-items: center;
  font-weight: bold;
  /* width: 100%; */
  background-color: hsla(160, 100%, 37%, 0.2);
  height: 100px;
  display: flex;
  padding: 10px;
  border-radius: 0px 0px 7px 7px;
}
nav a.router-link-exact-active {
  color: var(--color-text);
}
nav a.router-link-exact-active:hover {
  background-color: transparent;
}
nav a {
  display: inline-block;
  padding: 0 1rem;
  border-left: 1px solid var(--color-border);
}
nav a:first-of-type {
  border: 0;
}
</style>
