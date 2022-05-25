<template>
  <div class="footer m-64">
    <div class="social-list">
      <a href="#"><i class="ti-facebook"></i></a>
      <a href="#"><i class="ti-instagram"></i></a>
      <a href="#"><i class="ti-pinterest"></i></a>
      <a href="#"><i class="ti-twitter"></i></a>
      <a href="#"><i class="ti-linkedin"></i></a>
      <a href="#"><i class="ti-youtube"></i></a>
    </div>
    <p>Powered by <a href="#">w3.css</a></p>
  </div>
</template>

<style scoped>
.footer{
  text-align: center;
}
.footer .social-list a{
  text-decoration: none;
  color: var(--dark);
  font-size: 25px;
  padding: 0 8px;
}
.footer .social-list a:hover{
  opacity: 0.6;
}
.footer p{
  margin: 15px 0;
  opacity: 0.6;
}
.footer p a{
  color: var(--dark);
} 
</style>
