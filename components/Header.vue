<template>
  <header>
    <nav>
      <ul>
        <li><nuxt-link to="/" class="button--green">Home</nuxt-link></li>
        <li><nuxt-link to="/recipes" class="button--grey">Recipes</nuxt-link></li>
        <li><nuxt-link to="/about" class="button--grey">About</nuxt-link></li>
      </ul>
    </nav>
  </header>
</template>

<style scoped>
header {
  margin-top: 10px;
  width: 100%;
  height: 30px;
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: wheat;
}
ul {
  list-style: none;
  padding: 0;
  margin: 0;
  display: flex;
  justify-content: center;
  align-items: center;
}
li {
  margin: 0 10px;
}
</style>
