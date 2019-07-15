<template>
  <div class="post-item">
    <div class="content">
      <div class="post">
        <h1 class="post-title">{{post.title}}</h1>
        <div class="post-background">
          <a :href="post.url">
            <img class="post-image" :src="post.thumbnail" />
          </a>
          <div class="post-description">
            <p>{{post.description}}</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.content {
  padding: 16px;
}

.post {
  margin-top: 0px;
  color: white;
  z-index: -999;
}
.post .post-background {
  background-color: #a19fd0;
  position: relative;
}
.post h1 {
  padding: 3px;
  margin-bottom: 0px;
  background-color: #676ab2;
  border-top-right-radius: 2px;
  border-top-left-radius: 2px;
  font-size: 80%;
  text-align: center;
  font-weight: bold;
  width: 60%;
}
.post img {
  padding: 10px;
  display: block;
  margin: auto;
  max-width: 100%;
  max-height: 100%;
  min-height: 100%;
  min-width: 100%;
}
.post .post-description {
  width: 100%;
  box-sizing: border-box;
  font-size: 90%;
  position: absolute;
  bottom: 0px;
  background-color: rgba(0, 0, 0, 0.342);
}
.post .post-description p {
  padding-left: 15px;
  padding-right: 15px;
}

@media (min-width: 1000px) {
  .post h1 {
    font-size: 130%;
  }
  .post p {
    font-size: 130%;
  }
}

@media (min-width: 1200px) {
  .post p {
    font-size: 160%;
  }
}
</style>

<script>
export default {
  name: "PostItem",
  props: ["post"]
};
</script>