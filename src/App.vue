<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
import HelloWorld from './components/HelloWorld.vue'
import TheHeader from './components/TheHeader.vue';
var type = "x";
var array = [
  {
    "id": 1,
    "name": "Leanne Graham",
    "username": "Bret",
    "email": "Sincere@april.biz",
    "address": {
      "street": "Kulas Light",
      "suite": "Apt. 556",
      "city": "Gwenborough",
      "zipcode": "92998-3874",
      "geo": {
        "lat": "-37.3159",
        "lng": "81.1496"
      }
    },
    "phone": "1-770-736-8031 x56442",
    "website": "hildegard.org",
    "company": {
      "name": "Romaguera-Crona",
      "catchPhrase": "Multi-layered client-server neural-net",
      "bs": "harness real-time e-markets"
    }
  },
  {
    "id": 2,
    "name": "Ervin Howell",
    "username": "Antonette",
    "email": "Shanna@melissa.tv",
    "address": {
      "street": "Victor Plains",
      "suite": "Suite 879",
      "city": "Wisokyburgh",
      "zipcode": "90566-7771",
      "geo": {
        "lat": "-43.9509",
        "lng": "-34.4618"
      }
    },
    "phone": "010-692-6593 x09125",
    "website": "anastasia.net",
    "company": {
      "name": "Deckow-Crist",
      "catchPhrase": "Proactive didactic contingency",
      "bs": "synergize scalable supply-chains"
    }
  }]
var imgAlt = 'OneImage';
var src = "https://www.jacalculei.com.br/wp-content/uploads/2022/02/O-que-e%CC%81-Pessoa-Juri%CC%81dica-.png"
var home = true;
var classVar = {
  'title': true,
  'emerson': home ? true : false
}

</script>

<template>
  <TheHeader />
  <div v-if="type === 'admin'">Admin</div>
  <div v-else-if="type === 'marketing'">Marketing</div>
  <div v-else>Client</div>
  <div v-for="local in array" :key="local.id" class="toDo">
    {{ local.company.name }}
    <img :src="src" :alt="imgAlt">
  </div>

  <h1 :class="classVar">
    Curso vue.js
  </h1>
  <p :class="['text','title']">
    Lorem ipsum dolor sit, amet consectetur adipisicing elit. Facere perferendis saepe minima maiores suscipit repellat optio consequatur natus quod a. Accusantium eaque cum beatae molestias veniam quae magnam qui dignissimos!
  </p>


  <header>
    <img alt="Vue logo" class="logo" src="@/assets/logo.svg" width="125" height="125" />

    <div class="wrapper">
      <HelloWorld msg="You did it!" />
      <nav>
        <RouterLink to="/">Home</RouterLink>
        <RouterLink to="/about">About</RouterLink>
      </nav>
    </div>
  </header>

  <RouterView />
</template>

<style scoped>
.title {
  background-color: yellow;
  color: black
}

.toDo {
  background-color: rgb(38, 9, 156);
  color: white;
  margin: 2px 0px 0px 0px;
}
.emerson{
  background-color: pink;
}

header {
  line-height: 1.5;
  max-height: 100vh;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

nav {
  width: 100%;
  font-size: 12px;
  text-align: center;
  margin-top: 2rem;
}

nav a.router-link-exact-active {
  color: var(--color-text);
}

nav a.router-link-exact-active:hover {
  background-color: transparent;
}

nav a {
  display: inline-block;
  padding: 0 1rem;
  border-left: 1px solid var(--color-border);
}

nav a:first-of-type {
  border: 0;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }

  nav {
    text-align: left;
    margin-left: -1rem;
    font-size: 1rem;

    padding: 1rem 0;
    margin-top: 1rem;
  }
}
</style>
