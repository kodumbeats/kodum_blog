<template lang="pug">
html
  body
    h1 > kodum_blog
      span.cursor |
    <br>
  <Nuxt />
  footer.
    #[a(href="https://leckemby.me") about]
    #[a(href="mailto: brandon.leckemby@gmail.com") email]
    #[a(href="https://www.linkedin.com/in/brandonleckemby") linkedin]
    #[a(href="https://github.com/kodumbeats") github]
    <br> &#169; 2020 kodumdotnet
</template>

<style scoped>
@import url('https://cdn.jsdelivr.net/npm/@exampledev/new.css@1.1.2/new.min.css');
@import url('https://newcss.net/theme/terminal.css');
body {
  padding: 0;
}
.cursor {
  animation: blinker 1.2s step-end infinite;
}
@keyframes blinker {
  50% {
    opacity: 0;
  }
}
footer {
  text-align: center;
  padding-top: 3em;
}
</style>
