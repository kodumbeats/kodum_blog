---
title: vercel.txt
---

I probably lose a bit of job security to [JAMStack](https://jamstack.org) apps, as they "[remove] the requirement to manage or run web servers." However, JAMStack apps are incredibly pleasant to build, performant out-of-the-box, and ensure the necessary processing requirements of the app are offloaded to everything _but_ the end user. This blgo now runs on the same stack, rebuilt using the [`@nuxt/content`](https://content.nuxtjs.org/) module and hosted on [Vercel](https://vercel.com). And my goodness, Vercel is a gem.

I use git repos everywhere*, so all Vercel required of me was a Github auth, my FQDN, and `nuxt generate` as a build command, and this blog was online, built and hosted in about a minute. I had to change git repos for a refactor, and Vercel built from the very next commit. I wrote out a post cataloguing my adventures with Vercel, but it became too redundant compared to the easy-to-understand [docs](https://vercel.com/docs). 

Need to demo a PR? Have a staging branch? Just push to 'em and watch Vercel build and serve your changes. Please don't push changes to your main branch repeatedly, even though it's a bad idea. _Of coourrrsee I responsibly develop :cough:_.

When I wish to somehow optimize the web service itself, my syadmin hands sorely miss running the code myself. My calendar, however, appreciates the support of maintenance.

But seriously, for all of my fellow indie hackers looking for a way to build new stuff, give your project the professionalism it deserves with a framework-framework like Next.js or Nuxt.js, hop on the JAMStack train, and slap it up on Vercel. 

_P.S. Only in my dreams is this post sponsored. Vercel, if you read this, I'd love to work with y'all. Hit me up._
  
<div class="footnote">&nbsp;* even in places I shouldn't, but :shrug:</div>
