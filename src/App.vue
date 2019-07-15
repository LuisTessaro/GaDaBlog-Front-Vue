<template>
  <div id="app">
    <Header></Header>
    <Posts class="posts" v-bind:posts="posts"></Posts>
    <Footer></Footer>
  </div>
</template>

<script>
import axios from "axios";
import Posts from "./components/Posts";
import Header from "./components/layout/Header";
import Footer from "./components/layout/Footer";

export default {
  name: "app",
  components: {
    Posts,
    Header,
    Footer
  },
  data() {
    return {
      posts: []
    };
  },
  created() {
    axios.get("http://localhost:3000/api/posts").then(res => {
      this.posts = res.data;
    });
  }
};
</script>

<style>
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  margin: 0;
  padding: 0;
  background-color: white;
  color: darkblue;
  font-size: 18px;
  font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
}
.posts {
  margin: 60px auto 60px auto;
}

@media (min-width: 600px) {
  .posts {
    width: 80%;
  }
}

@media (min-width: 800px) {
  .posts {
    width: 70%;
  }
}

@media (min-width: 1000px) {
  .posts {
    width: 60%;
  }
}

@media (min-width: 1200px) {
  .posts {
    width: 50%;
  }
}
</style>