<template>
  <article>
    <!-- <h1>{{ article.title }}</h1>
    <p>{{ article.description }}</p>
    <img :src="article.img" :alt="article.alt" />
    <p>Article last updated: {{ formatDate(article.updatedAt) }}</p> -->
    <pre> {{ article }} </pre>
    <nuxt-content :document="article" />
  </article>
</template>

<script>
export default {
  async asyncData({ $content, params }) {
    const article = await $content('articles', params.slug).fetch()
    return { article }
  },
  methods: {
    formatDate(date) {
      const options = { year: 'numeric', month: 'long', day: 'numeric' }
      return new Date(date).toLocaleDateString('en', options)
    },
  },
}
</script>
<style>
.nuxt-content h2 {
  font-weight: bold;
  font-size: 28px;
  color: red;
}
.nuxt-content h3 {
  font-weight: bold;
  font-size: 22px;
  color: red;
}
.nuxt-content p {
  margin-bottom: 20px;
}
</style>
