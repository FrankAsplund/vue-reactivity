<script setup>
import { RouterLink, RouterView } from "vue-router";
</script>
<!-- src="@/assets/logo.svg" -->

<template>
  <nav>
    <div class="navbar">
      <img
        alt="logo"
        class="logo"
        src="https://8128125.fs1.hubspotusercontent-na1.net/hub/8128125/hubfs/onify-logo-white-1.png?width=136&name=onify-logo-white-1.png"
        width="136"
        height="50"
      />
      <h1>Onify form test</h1>
      <div class="router">
        <RouterLink to="/">Home</RouterLink>
        <RouterLink to="/about">About</RouterLink>
        <RouterLink to="/users">Users</RouterLink>
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
  height: 80px;
  display: flex;
  padding: 15px;
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
