<template>
  <div id="slider">
      <div class="slider__content">
        <h1 class="slider__heading">Los Angeles</h1>
        <p class="slider__text">We had the best time playing at Venice Beach!</p>
      </div>
  </div>
</template>
<style scoped>
#slider{
  margin-top: 46.5px;
  width:100%;
  padding-top: 50%;
  background: url(../assets/imgs/slide-1.jpg) top center / cover no-repeat;
  position: relative;
}
#slider .slider__content{
  color: var(--light); 
  width: 100%;
    text-align:center ;
    position: absolute;
    bottom: 47px;
    left: 50%;
    transform: translateX(-50%);

}
#slider .slider__content .slider__heading{
  font-weight: 400;
  font-size: 24px;
  margin-bottom: 25px;
}


</style>
