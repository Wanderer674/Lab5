<!-- <script setup>
import HelloWorld from './components/HelloWorld.vue'
import TheWelcome from './components/TheWelcome.vue'
</script>

<template>
  <header>
    <img alt="Vue logo" class="logo" src="./assets/logo.svg" width="125" height="125" />

    <div class="wrapper">
      <HelloWorld msg="You did it!" />
    </div>
  </header>

  <main>
    <TheWelcome />
  </main>
</template>

<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
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
}
</style> -->

<!-- <script setup>
import Bai1 from './components/Bai1.vue';
</script>
<template>
<Bai1/>
</template> -->

<!-- <script setup>
import Bai2 from './components/Bai2.vue';
</script>
<template>
<Bai2/>
</template> -->

<!-- <script setup>
import Bai3 from './components/Bai3.vue';
</script>
<template>
<Bai3/>
</template> -->

<template>
  <div id="app">
      <h1>Ứng dụng blog nhở với Vue.js</h1>   
      <CreatePost @add-post="addPost" />
      <PostList :posts="posts" />
  </div>
</template>

<script setup>

  import {ref} from 'vue'
  import CreatePost from './components/Createpost.vue'
  import PostList from './components/PostList.vue'

  const posts = ref([])

  function addPost(post){
    posts.value.push(post)
  }
</script>

<style>
  #app{
    max-width: 800px;
    margin: 0 auto;
    padding: 20px;
  }
</style>