<template>
  <ul class="container">
    <li>
      <h2>> {{ blogpost.title }} <span class="cursor">_</span></h2>
      <hr class="hr2" />
      <h5>--> {{ formatDate(blogpost.createdAt) }}</h5>
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
li {
  color: #eeeeee;
  font-family: 'Cairo', sans-serif;
  margin-left: 2rem;
  margin-right: 2rem;
  p {
    margin-bottom: 1rem;
  }
}
.hr2 {
  border: 1px solid #721d53;
}
h2 {
  font-size: 2rem;
}
h5 {
  font-size: 1rem;
  margin-left: 1.5rem;
}
p {
  font-size: 1.2rem;
  line-height: 1.6rem;
  padding-bottom: 1.6rem;
}
a {
  color: #9100f0;
}
code {
  font-size: 0.9rem;
  font-family: 'Changa', sans-serif;
  color: #e9fbef;
  background-color: #701351;
  border-radius: 4px;
}
.footnote {
  font-size: 0.8rem;
  line-height: 1rem;
}
ul {
  list-style-type: none;
}
.container {
  height: 100%;
}
</style>
