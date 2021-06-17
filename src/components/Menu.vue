<template>
  <div class="menu">
    <div class="dropdown">
      <div class="dropbtn">
        <img src="../assets/icons/foods_drink.svg" class="menu-icon" /><span>Health Foods & Drinks</span>
      </div>
      <div class="dropdown-content">
        <a href="#">Link 1</a>
        <a href="#">Link 2</a>
        <a href="#">Link 3</a>
      </div>
    </div>
    <div class="dropdown">
      <div class="dropbtn">
        <img src="../assets/icons/special_hempres.svg" class="menu-icon" /><span>Home Appliances</span>
      </div>
      <div class="dropdown-content">
        <a href="#">Link 1</a>
        <a href="#">Link 2</a>
        <a href="#">Link 3</a>
      </div>
    </div>
    <div class="dropdown">
      <div class="dropbtn">
        <img src="../assets/icons/children_an_beby.svg" class="menu-icon" /><span>Mom &<br />Baby</span>
      </div>
      <div class="dropdown-content">
        <a href="#">Link 1</a>
        <a href="#">Link 2</a>
        <a href="#">Link 3</a>
      </div>
    </div>
    <div class="dropdown">
      <div class="dropbtn">
        <img src="../assets/icons/icon_personal_care.svg" class="menu-icon" /><span>Personal<br />Care</span>
      </div>
      <div class="dropdown-content">
        <a href="#">Link 1</a>
        <a href="#">Link 2</a>
        <a href="#">Link 3</a>
      </div>
    </div>
    <div class="dropdown">
      <div class="dropbtn">
        <img src="../assets/icons/sports_nutrition.svg" class="menu-icon" /><span>Sports & Nutrition</span>
      </div>
      <div class="dropdown-content">
        <a href="#">Link 1</a>
        <a href="#">Link 2</a>
        <a href="#">Link 3</a>
      </div>
    </div>
    <div class="dropdown">
      <div class="dropbtn">
        <img src="../assets/icons/supplement_n_vitamin.svg" class="menu-icon" /><span>Vitamins & Supplements</span>
      </div>
      <div class="dropdown-content">
        <a href="#">Link 1</a>
        <a href="#">Link 2</a>
        <a href="#">Link 3</a>
      </div>
    </div>
    <div class="dropdown">
      <div class="dropbtn">
        <img src="../assets/icons/weight_management.svg" class="menu-icon" /><span>Weight Management</span>
      </div>
      <div class="dropdown-content">
        <a href="#">Link 1</a>
        <a href="#">Link 2</a>
        <a href="#">Link 3</a>
      </div>
    </div>
    <div id="right-section">
      <a href="#" class="brands-sale brands"><img src="../assets/icons/brand_image_header.svg" class="menu-icon" /> Brands</a>
      <a href="#" class="brands-sale sales"><img src="../assets/icons/icon_discount_header.svg" class="menu-icon" /> Sale</a>
    </div>
  </div>
</template>

<script>
</script>

<style scoped>
.menu {
  overflow: hidden;
  width: var(--container-size);
  margin: 0 auto;
}

.menu a {
  float: left;
  color: grey;
  text-align: left;
  text-decoration: none;
}

.dropdown {
  float: left;
  overflow: hidden;
  cursor: pointer;
}

.dropbtn {
  display: grid;
  grid-template-columns: 1fr 2fr;
  width: 150px;
}

.dropbtn span {
  font-size: 11px;
  margin-top: 5px;
}

.dropdown .dropbtn {
  font-size: 16px;
  border: none;
  outline: none;
  color: grey;
  padding: 14px 16px;
  background-color: inherit;
  font-family: inherit;
  margin: 0;
}

.menu-icon {
  height: 40px;
}

.dropdown-content {
  display: none;
  position: absolute;
  background-color: #f9f9f9;
  width: 300px;
  z-index: 1;
}

.dropdown-content a {
  float: none;
  color: black;
  padding: 12px 16px;
  text-decoration: none;
  display: block;
  text-align: left;
}

.dropdown-content a:hover {
  background-color: #ddd;
}

.dropdown:hover .dropdown-content {
  display: block;
}

.brands-sale {
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 10px;
  font-weight: bold;
}

#right-section .sales {
  color: rgb(231, 80, 80);
}

#right-section .brands {
  color: var(--secondary-color);
}
</style>
