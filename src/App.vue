<template>
  <div id="app">
    <header>
      <nav>
        <router-link to="/">Home</router-link> |
        <router-link to="/projects">Projects</router-link> |
        <router-link to="/contact">Contact</router-link>
      </nav>
    </header>
    <main>
      <router-view></router-view>
    </main>
  </div>
</template>

<style>
body {
  font-family: Arial, sans-serif;
  margin: 0;
}
header {
  background-color: #333;
  padding: 1rem;
}
header nav a {
  color: white;
  margin-right: 1rem;
  text-decoration: none;
}
header nav a.router-link-exact-active {
  font-weight: bold;
  text-decoration: underline;
}
main {
  padding: 2rem;
}
</style>
