<template>
  <footer id="footer">
    <div class="footer-top">
      <ul>
        <li class="title">Information</li>
        <li><a href="#">Home</a></li>
        <li><a href="#">Products</a></li>
        <li><a href="#">Store Location</a></li>
      </ul>
      <ul>
        <li><a href="#">Member</a></li>
        <li><a href="#">Comfirm Payment</a></li>
        <li><a href="#">Order History</a></li>
      </ul>
      <ul>
        <li class="title">Operational Hours</li>
        <li><a href="#">Monday-Friday, 08.00 - 17.00 WIB</a></li>
        <li class="title">Customer Care</li>
        <li><a href="#"><i class="fab fa-whatsapp" /> 0812-1989-3252</a></li>
        <li><a href="#"><i class="fas fa-phone-alt" /> 021 - 5665 794</a></li>
        <li><a href="#"><i class="far fa-envelope" /> support@naturalfarm.id</a></li>
      </ul>
      <ul>
        <li class="title">Social Media</li>
        <li><a href="#"><img src="../assets/icons/instagram.svg" class="social-media-icons"> naturalfarm.id</a></li>
        <li><a href="#"><img src="../assets/icons/facebook.svg" class="social-media-icons"> Natural Farm</a></li>
        <li><a href="#"><img src="../assets/icons/twitter.svg" class="social-media-icons"> @naturalfarm</a></li>
      </ul>
    </div>
    <div class="footer-bottom">Copyright 2021 by <b>Natural Farm</b>, Jakarta - Indonesia</div>
  </footer>
</template>

<script>
</script>

<style scoped>
#footer {
  background: ghostwhite;
  border-top: 1px solid gainsboro;
}

.footer-top {
  width: var(--container-size);
  display: grid;
  grid-template-columns: 1fr 1fr 1fr 1fr;
  padding: 20px;
  margin: 0 auto;
}

.footer-top ul li {
  list-style: none;
  margin: 3px 0;
  font-size: 14px;
}

.footer-top ul li a {
  color: #0a0a0a;
  font-size: 12px;
}

.title {
  font-weight: bold;
}

.social-media-icons {
  height: 14px;
}

.footer-bottom {
  text-align: center;
  background: var(--secondary-color);
  color: white;
  padding: 5px 0;
  font-size: 15px;
}

@media (max-width: 720px) {
  .footer-top {
    grid-template-columns: 1fr 1fr;
  }

  .footer-top ul {
    margin-top: 10px;
  }
}
</style>
