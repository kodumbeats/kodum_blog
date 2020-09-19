<template>
  <div class="wholething">
    <mq-layout mq="md+">
      <div class="header">
        <nuxt-link to="/blog"
          ><img class="header" src="/dotmeslashblog_4x.png"
        /></nuxt-link>
      </div>
    </mq-layout>
    <mq-layout mq="sm">
      <nuxt-link to="/blog"
        ><h1 class="smallheader">kodum_blog _</h1></nuxt-link
      >
      <hr class="hr1" />
    </mq-layout>
    <Nuxt />
    <footer>
      <nuxt-link to="/">home</nuxt-link>
      <a href="mailto: brandon.leckemby@gmail.com">email</a>
      <a href="https://github.com/kodumbeats">github</a>
      <a href="https://www.linkedin.com/in/brandonleckemby">linkedin</a>
      <br />
      &#169; 2020 kodumdotnet
    </footer>
  </div>
</template>

<style scoped>
.wholething {
  background-color: #000000;
}
h1 {
  color: #ffffff;
  font-family: 'Changa', sans-serif;
  font-size: 2.8rem;
  margin-left: 10px;
}
a {
  font-family: 'Changa', sans-serif;
}
.header {
  display: block;
  margin: 0 auto 1rem 4rem;
  padding: 1rem 0;
  height: 200px;
}
.smallheader {
  padding-left: 1rem;
}
.hr1 {
  border: 2px solid #222579;
}
footer {
  text-align: center;
  padding-top: 3em;
}
</style>
