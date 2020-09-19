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
h1,
h2,
h3,
h4,
h5,
h6 {
  color: #ffffff;
  font-family: 'Changa', sans-serif;
}
p,
li {
  color: #eeeeee;
  font-family: 'Cairo', sans-serif;
}
h2 {
  font-size: 24px;
}
h5 {
  font-size: 10px;
  margin-bottom: 1em;
}
p,
code {
  font-size: 12px;
}
a {
  color: #9100f0;
}
code {
  font-family: 'Changa', sans-serif;
  color: #e9fbef;
  background-color: #701351;
  border-radius: 4px;
}
li {
  font-size: 8px;
}
ul {
  list-style-type: none;
}
</style>
