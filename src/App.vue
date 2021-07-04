<template>
  <h1>Meal prep app</h1>
  <div class="recipe">
    <h3> {{ recipe.name }} </h3>
    <ul>
      <li v-for="ingredient of recipe.ingredients" :key="ingredient">
        {{ ingredient }}
      </li>
    </ul>
  </div>
</template>

<script>

export default {
  name: 'App',
  components: {
    // this will hold components
  },
  data() {
    return {
      recipe
    }
  }
}

// Dummy recipe for dev purposes, will be removed later
const recipe = {
  name: 'Vegan hot dog',
  ingredients: ['onion', 'garlic', 'cooked pinto beans', 'water', 'soy sauce', 'tomato paste', 'rolls'],
  recipeUrl: 'https://blog.fatfreevegan.com/2014/07/homemade-veggie-dogs.html',
  labels: []
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  max-width: 800px;
}

.recipe {
  background-color: #2c3e50;
  color:#ddd;
  margin: 10px;
  padding: 10px;
}
</style>
