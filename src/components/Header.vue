<template>
  <header id="header">
    <div class="container">
      <ul class="left-contents">
        <li>
          <a href="#">Official natural farm di lokasi terdekat anda</a>
        </li>
      </ul>
      <ul class="right-contents">
        <li>
          <a href="#"><img src="../assets/icons/blog_home.svg" /> Blog</a>
        </li>
        <li>
          <a href="#"><img src="../assets/icons/promotion.svg" /> Promotions</a>
        </li>
        <li>
          <a href="#"><img src="../assets/icons/all_products.svg" /> All Products</a>
        </li>
      </ul>
    </div>
  </header>
</template>

<script>
</script>

<style scoped>
#header {
  background-color: var(--primary-color);
  color: white;

}

.container {
  width: var(--container-size);
  display: grid;
  grid-template-columns: 1fr 1fr;
  margin: 0 auto;
}

#header ul li {
  display: inline-block;
  padding: 0 10px;
  list-style: none;
}

#header ul li a {
  color: white;
}

#header ul li a img {
  width: 17px;
}

.right-contents {
  text-align: right;
  font-weight: bold;
  font-size: 14px;
}

.left-contents {
  text-align: left;
  padding-left: 0;
}

.left-contents li a {
  font-size: 14px;

}
</style>
