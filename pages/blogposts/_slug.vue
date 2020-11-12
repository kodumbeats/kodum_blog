<template>
  <ul>
    <li>
      <h2>> {{ blogpost.title }} <span class="cursor">_</span></h2>
      <hr class="hr2" />
      <h3>--> {{ formatDate(blogpost.createdAt) }}</h3>
      <nuxt-content :document="blogpost" />
    </li>
  </ul>
</template>

<script>
export default {
  async asyncData({ $content, params }) {
    const blogpost = await $content('blogposts', params.slug).fetch()
    return { blogpost }
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
