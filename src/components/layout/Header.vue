<template>
  <div>
    <header>
      <div class="navbar">
        <a href="#news">NEWS</a>
        <a href="#contact">CONTACT US</a>
        <a class="right" href="#contact">
          <i class="fas fa-beer"></i>
        </a>
      </div>
    </header>
  </div>
</template>
<style scoped>
.navbar {
  overflow: hidden;
  background-color: #333;
  z-index: 999;
  position: fixed;
  top: 0;
  width: 100%;
}
.navbar a {
  float: left;
  display: block;
  color: #f2f2f2;
  text-align: center;
  padding: 14px 16px;
  text-decoration: none;
  font-size: 17px;
}
.navbar a.right {
  float: right;
}
.navbar a:hover {
  background: #ddd;
  color: black;
}
</style>
<script>
export default {
  name: "Header"
};
</script>