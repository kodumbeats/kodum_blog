---
title: kodoto.pug
createdAt: '2020-05-20'
updatedAt: '2020-05-20'
---

In the neverending pursuit of increased productivity, I always seek out new tools and services that align with my laziness. [Ultralist](https://github.com/ultralist/ultralist) stands out as a favorite of mine, but ultralist treats todolists like sqlite3 databases, writing json files locally. Nevertheless, an ultralist file, stored in version control, has kept my projects structured and absent of "whatnext" syndrome.

Since todolists live near my heart, a personal todolist API would serve both as an ultralist replacement (with a CLI tool in the works) and aggregator of my many lists floating on my local [git](https://github.com/go-gitea/gitea) server. While the API was born using [restify](https://github.com/restify/node-restify), project needs drove the API to pure [Express.js](https://expressjs.com/). While in very early alpha, the project served as a great diving board into the ocean of web development. ([source](https://glitch.com/edit/#!/kotodo))
