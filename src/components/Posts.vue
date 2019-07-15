<template>
  <div class="posts">
    <div v-bind:key="post.id" v-for="post in posts">
      <PostItem v-bind:post="post"></PostItem>
    </div>
  </div>
</template>
<style scoped>
</style>
<script>
import PostItem from "./PostItem";

export default {
  name: "Posts",
  props: ["posts"],
  components: {
    PostItem
  }
};
</script>