<template>
  <nav id="navbar">
    <div class="container">
      <img src="../assets/img/logo_naturalfarm.svg" alt="logo" class="navbar-logo" />
      <div class="search-container">
        <input type="text" class="input-container" placeholder="Search Product..." />
        <i class="fas fa-search"></i>
      </div>
      <a href="#"><img src="../assets/icons/shopping_icon_header.svg" alt="cart" class="cart-icon" /></a>
      <button class="btn-login">Login</button>
      <button class="btn-registration">VIP Member re-Registration</button>
      <div></div>
      <div class="suggestion-menu">
        <ul>
          <li><a href="#">Vitamin C</a></li>
          <li><a href="#">Manukai Honey</a></li>
          <li><a href="#">Wellness</a></li>
          <li><a href="#">Zinc</a></li>
          <li><a href="#">Omega</a></li>
          <li><a href="#">Vitamin D</a></li>
          <li><a href="#">Vitamin E</a></li>
        </ul>
      </div>
    </div>
  </nav>
</template>

<script>
</script>

<style scoped>
#navbar {
  border-bottom: 1px solid gainsboro;
}

.container {
  margin: 0 auto;
  padding: 15px 0;
  width: var(--container-size);
  display: grid;
  grid-template-columns: 3fr 9fr 1fr 1fr 4fr;
}

#navbar .navbar-logo {
  height: 40px;
}

#navbar .cart-icon {
  height: 40px;
}

.search-container {
  display: flex;
  background-color: var(--grey);
  flex-direction: row;
  border: 1px solid rgba(0, 0, 0, 0.3);
  width: 95%;
  padding: 10px;
  height: 40px;
  border-radius: 5px;
}

input[type=text]:focus {
  outline: none;
}

.input-container {
  flex: 1;
  background-color: var(--grey);
  border: none;
}

.btn-login {
  background: transparent;
  border: none;
  font-size: 16px;
  padding: 0;
  margin-right: 15px;
  cursor: pointer;
}

.btn-registration {
  background: var(--secondary-color);
  border: none;
  color: white;
  height: 40px;
  border-radius: 5px;
  font-size: 16px;
  cursor: pointer;
}

.suggestion-menu ul li {
  display: inline-block;
  list-style: none;
  text-align: left;
}

.suggestion-menu ul li a {
  color: grey;
  padding: 0 10px;
  font-size: 11px;
}

.suggestion-menu ul li a:hover {
  color: var(--primary-color);
}
</style>
