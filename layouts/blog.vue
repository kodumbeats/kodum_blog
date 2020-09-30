<template>
  <div class="wholething">
    <mq-layout mq="md+">
      <nuxt-link to="/"><h1 class="bigheader">kodum_blog _</h1></nuxt-link>
    </mq-layout>
    <mq-layout mq="sm">
      <nuxt-link to="/"><h1 class="smallheader">kodum_blog _</h1></nuxt-link>
    </mq-layout>
    <hr class="hr1" />
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
h1,
h2,
h3,
h4,
h5,
h6 {
  color: #ffffff;
  font-family: 'Changa', sans-serif;
}
h1 {
  padding-left: 1rem;
}
h2 {
  font-size: 2rem;
}
h5 {
  font-size: 1rem;
  margin-left: 1.5rem;
}
a {
  font-family: 'Changa', sans-serif;
  color: #9100f0;
}
code {
  font-size: 0.9rem;
  font-family: 'Changa', sans-serif;
  color: #e9fbef;
  background-color: #701351;
  border-radius: 4px;
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
p {
  font-size: 1.2rem;
  line-height: 1.6rem;
  padding-bottom: 1.6rem;
}
ul {
  list-style-type: none;
}
.bigheader {
  font-size: 3.5rem;
}
.smallheader {
  font-size: 2.5rem;
}
.hr1 {
  border: 0;
  height: 2px;
  background: #333;
  background-image: linear-gradient(to right, #000, #fff, #000);
}
.hr2 {
  border: 1px solid #721d53;
}
.footnote {
  font-size: 12px;
  line-height: 50%;
}
footer {
  text-align: center;
  padding-top: 3em;
}
</style>
