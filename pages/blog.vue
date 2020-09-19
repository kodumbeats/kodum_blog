<template>
  <ul>
    <li v-for="blog of blogposts" :key="blog.title">
      <h2>
        >
        <nuxt-link :to="blog.path" class="titlelink">
          {{ blog.title }}
        </nuxt-link>
        <span class="cursor">_</span>
      </h2>
      <hr class="hr2" />
      <h5>--> {{ formatDate(blog.createdAt) }}</h5>
      <nuxt-content :document="blog" />
    </li>
  </ul>
</template>

<script>
export default {
  async asyncData({ $content, params }) {
    const blogposts = await $content('blogposts')
      .only(['title', 'createdAt', 'body', 'path'])
      .sortBy('createdAt', 'desc')
      .limit(5)
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
/* Need to manually keep this matching with blogposts/_slug until i can fix it */
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
.titlelink {
  color: #eeeeee;
  text-decoration: none;
}
.titlelink:hover {
  color: #9100f0;
  text-decoration: underline;
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
</style>
