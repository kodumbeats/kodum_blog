<template>
  <ul>
    <li v-for="blog of blogposts" :key="blog.title">
      <h2>> {{ blog.title }}</h2>
      <h5>{{ formatDate(blog.createdAt) }}</h5>
      <nuxt-content :document="blog" />
    </li>
  </ul>
</template>

<script>
export default {
  async asyncData({ $content, params }) {
    const blogposts = await $content('blogposts')
      .only(['title', 'createdAt', 'body'])
      .sortBy('createdAt', 'desc')
      .limit(3)
      .fetch()
    return { blogposts }
  },
  methods: {
    formatDate(date) {
      const d = new Date(date)
      const year = d.getFullYear()
      const month = d
        .toLocaleString('default', { month: 'short' })
        .toLowerCase()
      let day = d.getDate().toString()
      if (day.length < 2) {
        day = '0' + day
      }
      return [year, month, day].join('_')
    },
  },
  layout: 'blog',
}
</script>

<style>
ul {
  list-style-type: none;
}
</style>
