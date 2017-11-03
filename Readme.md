# Test for Crowdcube

## Installation

First you have to install the backend
``` shell
git clone https://github.com/ellipticaldoor/cube-backend
cd cube-backend
npm install
npm start
```

Now install the fronted
``` shell
git clone https://github.com/ellipticaldoor/cube-frontend
cd cube-frontend
npm install
npm run dev
```

And should be able to see the app running.


## About

This project is divided in two parts. First the backend, a [node](https://nodejs.org/en/) app using the framework [feathersjs](https://feathersjs.com/).

# Backend

I decided to use the framework feathersjs because is a tool that allows fast development. This is thanks to its cli generator,

Other advantages of using feathers are:
  - Modular services
  - Use almost any database available (postgres, mongodb, etc...)
  - Full CRUD api generator based on database model
  - [A querying client](https://docs.feathersjs.com/api/databases/querying.html)
  - Real time queries

I decided to use [nedb](https://github.com/louischatriot/nedb) because it saves the database in a local file. I scraped some data from the website [https://www.crowdcube.com/investments](https://www.crowdcube.com/investments) and added it to the backend repo.

# Frontend

In the fronted I used [Vue](https://vuejs.org/) with [feather-vuex](https://github.com/feathers-plus/feathers-vuex) (integrates the feathers services into [vuex](https://github.com/vuejs/vuex)).

The app it's a [PWA](https://en.wikipedia.org/wiki/Progressive_web_app) so all the content is cached in the browser using service workers, so the apps load faster the next time you visit it and also allows offline ussage.

For cleaner code I used [Prettier](https://github.com/prettier/prettier) (an opinionated code formatter), [SASS](http://sass-lang.com/) a CSS preprocessor and [Pug](https://pugjs.org/api/getting-started.html) an HTML preprocessor. I explained this choices [here in this post](https://ellipticaldoor.com/2017-07-26-simplifying-vue-js-development/) of my blog.

The app contains a basic example of component ussage, with sorting and a real-time connection to the database.
