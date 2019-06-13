<template>
  <nuxt-link :to="'/recipes/' + id">
    <article class="recipe">
      <div class="thumbnail" :style="{backgroundImage: 'url(' + thumbnail + ')'}"></div>
      <h1>{{title}}</h1>
      <p>{{previewText}}</p>
    </article>
  </nuxt-link>
</template>

<script>
export default {
  props: ['thumbnail', 'title', 'previewText', 'id']
}
</script>
