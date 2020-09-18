---
title: deno.txt
createdAt: '2020-05-21'
updatedAt: '2020-05-21'
---

Those in the Node.js world have been closely eyeing [deno](https://deno.land/) to learn the future of the secure-by-default js/ts runtime from none other than Ryan Dahl1, the creator of Node.js himself.

As a syadmin, the project goals resonate strongly with me: deno ships as a single binary, scripts have no access to the filesystem or networking by default, and the CLI tool includes some quality-of-life utilities like code formatting.

I wanted an environment to try out this new engine, but by default, Glitch only runs Node.js projects. After some trial-and-error (plus some help from geniuses in the community), I was able to implement deno in Glitch as a full Node.js replacement. The third-party plugin [Aqua](https://github.com/l2ig/aqua) felt very Express.js-esque, which enabled me to implement a basic web server in seconds: ([source](https://glitch.com/edit/#!/deno-kodumbeats))
  
[^1]: His [announcement post](https://deno.land/v1) is worth a read, especially the discussion of Deno's current limitations.
