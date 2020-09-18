<template lang="pug">
body
  include ~../../../assets/blogs/nuxt.pug
  include ~../../../assets/blogs/min.pug   
  include ~../../../assets/blogs/deno.pug
  include ~../../../assets/blogs/kotodo.pug   
  include ~../../../assets/blogs/pug.pug
</template>

<script>
export default {
  layout: 'blog',
}
</script>

<style scoped>
p.date {
  font-size: 0.9em;
  color: var(--nc-lk-1);
}
p.footnote {
  font-size: 0.8em;
  font-style: italic;
}
</style>
