<template>
  <section class="recipes">
    <Recipe
      v-for="recipe in recipes"
      :key="recipe.id"
      :thumbnail="recipe.thumbnail"
      :title="recipe.title"
      :id="recipe.id"
      :previewText="recipe.previewText" />
  </section>
</template>

<script>
import Recipe from '~/components/Recipe'
export default {
  components: {
    Recipe
  },
  asyncData() {
    return new Promise((resolve, reject) => {
      setTimeout(()=> {
        resolve({
          recipes: [
            {
              id: "1",
              title: "Delicious Pizza",
              previewText: "Awesome pizza!",
              thumbnail: "https://ichef.bbci.co.uk/food/ic/food_16x9_832/recipes/quick_pepperoni_pizza_64616_16x9.jpg"
            },
            {
              id: "2",
              title: "Seafood Salad",
              previewText: "Very tasty!",
              thumbnail: "https://ichef.bbci.co.uk/food/ic/food_16x9_832/recipes/hazelnutbuttergrille_89237_16x9.jpg"
            }
          ]
        })
      }, 1000)
    })
  }
}
</script>

<style>
a {
  text-decoration: none;
  color: black;
}
.recipes {
  margin-top: 70px;
  display: flex;
  flex-flow: row wrap;
  justify-content: center;
  align-items: center;
}
.recipe {
  box-sizing: border-box;
  width: 280px;
  padding: 8px;
  border: 1px solid #ccc;
  box-shadow: 0 2px 2px #aaa;
  margin: 10px;
}
.thumbnail {
  background-position: center;
  background-size: cover;
  width: 100%;
  height: 200px;
}
</style>
