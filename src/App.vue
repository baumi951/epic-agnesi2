<script setup lang="ts"></script>

<template>
  <header>
    <router-link
      v-for="route in $router.options.routes"
      :key="route.path"
      :to="route.path"
    >
      <p class="router-link">
        {{ route.name }}
      </p>
    </router-link>
  </header>
  <RouterView />
</template>

<style>
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

body {
  background-color: black;
  height: 100vh;
  align-items: center;
}

.router-link {
  margin-left: 12px;
  margin-right: 12px;
  text-transform: capitalize;
  display: inline-block;
  font-size: 15px;
  font-weight: 300;
}
</style>
