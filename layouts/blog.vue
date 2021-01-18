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

<style>
html {
  background-color: #0b0c10;
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
h3 {
  font-size: 1rem;
  margin-left: 1.5rem;
  padding-top: 0.5rem;
  padding-bottom: 0.5rem;
}
a {
  font-family: 'Changa', sans-serif;
  color: #ae3eff;
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
  padding-bottom: 1.2rem;
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
.wholething {
  max-width: 1024px;
  margin-left: auto;
  margin-right: auto;
}
.hr1 {
  border: 0;
  height: 2px;
  background-image: linear-gradient(to right, #fff, #0b0c10);
}
.titlelink {
  color: #eeeeee;
  text-decoration: none;
}
.titlelink:hover {
  color: #ae3eff;
  text-decoration: underline;
}
.hr2 {
  border: 0;
  height: 2px;
  background-image: linear-gradient(to right, #721d53, #0b0c10);
}
.footnote {
  font-size: 12px;
  line-height: 95%;
}
footer {
  text-align: center;
  padding-top: 3em;
  color: #eeeeee;
  font-family: 'Changa', sans-serif;
}
</style>
