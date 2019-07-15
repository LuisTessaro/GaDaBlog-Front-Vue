<template>
  <div>
    <footer>
      <div class="footer-navbar">
        <a href="#news">
          <i class="fab fa-google"></i>
        </a>
        <a class="right" href="#contact">About us</a>
      </div>
    </footer>
  </div>
</template>
<style scoped>
.footer-navbar {
  overflow: hidden;
  background-color: #333;
  z-index: 999;
  position: fixed;
  bottom: 0;
  width: 100%;
}
.footer-navbar a {
  float: left;
  display: block;
  color: #f2f2f2;
  text-align: center;
  padding: 14px 16px;
  text-decoration: none;
  font-size: 17px;
}
.footer-navbar a.right {
  float: right;
}
.footer-navbar a:hover {
  background: #ddd;
  color: black;
}
</style>
<script>
export default {
  name: "Footer"
};
</script>