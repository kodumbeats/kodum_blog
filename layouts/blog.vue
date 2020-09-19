<template lang="pug">
div.wholething
  div
    h1 > kodum_blog
      span.cursor |
  <Nuxt />
  footer.
    #[a(href="https://leckemby.me") about]
    #[a(href="mailto: brandon.leckemby@gmail.com") email]
    #[a(href="https://www.linkedin.com/in/brandonleckemby") linkedin]
    #[a(href="https://github.com/kodumbeats") github]
    <br> &#169; 2020 kodumdotnet
</template>

<style scoped>
.wholething {
  background-color: #000000;
}
h1 {
  color: #ffffff;
  font-family: 'Changa', sans-serif;
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
