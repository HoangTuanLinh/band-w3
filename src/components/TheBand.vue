<template>
  <div id="band">
    <div class="band m-64">
        <div class="main">
        <h2 class="band__heading heading">THE BAND</h2>
        <p class="band__sub-heading sub-heading"><i>We love music</i></p>
        <p class="band__desc">We have created a fictional band website. Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.</p>
        <div class="list-members">
          <div class="member">
            <p>Name</p>
            <img src="../assets/imgs/bandmember.jpg" alt="member">
          </div>
          <div class="member">
            <p>Name</p>
            <img src="../assets/imgs/bandmember.jpg" alt="member">
          </div>
          <div class="member">
            <p>Name</p>
            <img src="../assets/imgs/bandmember.jpg" alt="member">
          </div>
          <div class="clear"></div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>

</script>

<style>
.band{
  text-align: center;
}

.band .band__desc{
  text-align: justify;
    line-height: 1.4;
}
.list-members{
  margin: 32px 0;
}
.list-members .member{
  width: 33.333%;
  float: left;
}
.list-members .member p{
  margin: 15px 0;
  line-height: 1.4;
}
.list-members .member img{
  width: 154px;
  margin-bottom: 16px;
}
</style>
