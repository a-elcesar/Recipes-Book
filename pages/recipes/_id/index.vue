<template>
  <section class="single-recipe">
    <h1>{{recipe.title}}</h1>
    <div>
      <img class="recipe-image" :src="recipe.thumbnail" :alt="recipe.title" />
    </div>
    <p>{{recipe.descriptionText}}</p>
  </section>
</template>

<script>
export default {
  asyncData(context) {
    return new Promise((resolve, reject) => {
      setTimeout(()=> {
        resolve({
          recipe: [
            {
              id: "1",
              title: "Delicious Pizza",
              previewText: "Awesome pizza!",
              descriptionText: "This is really a delicious meal",
              thumbnail: "https://ichef.bbci.co.uk/food/ic/food_16x9_832/recipes/quick_pepperoni_pizza_64616_16x9.jpg"
            },
            {
              id: "2",
              title: "Seafood Salad",
              previewText: "Very tasty!",
              descriptionText: "This is really a delicious meal",
              thumbnail: "https://ichef.bbci.co.uk/food/ic/food_16x9_832/recipes/hazelnutbuttergrille_89237_16x9.jpg"
            }
          ].find(el => el.id === context.params.id)
        })
      }, 1000)
    })
  }
}
</script>

<style>
.single-recipe {
  display: flex;
  flex-flow: column;
  justify-content: center;
  align-items: center;
  text-align: center;
  padding: 30px;
}
.recipe-image {
  width: 100%;

}
</style>
