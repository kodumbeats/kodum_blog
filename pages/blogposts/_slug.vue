<template>
  <div>
    <h2>> {{ blogpost.title }}</h2>
    <h5>{{ blogpost.createdAt }}</h5>
    <nuxt-content :document="blogpost" />
  </div>
</template>

<script>
export default {
  async asyncData({ $content, params }) {
    const blogpost = await $content('blogposts', params.slug).fetch()
    return { blogpost }
  },
  layout: 'blog',
}
</script>
