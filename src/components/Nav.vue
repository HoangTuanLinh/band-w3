<template>
  <div id="header" :style="{height: `${height}`}">
    <ul id="nav">
      <li><a href="#" @click="changeHeight">Home</a></li>
      <li><a href="#band" @click="changeHeight">Band</a></li>
      <li><a href="#tour" @click="changeHeight">Tour</a></li>
      <li><a href="#contact" @click="changeHeight">Contact</a></li>
      <li><a href="#" @click="stopDefault">
        More
        <i class="ti-angle-down down-icon"></i>
        </a>
        <ul class="subnav">
          <li><a href="#" @click="changeHeight">Merchandise</a></li>
          <li><a href="#" @click="changeHeight">Extras</a></li>
          <li><a href="#" @click="changeHeight">Media</a></li>
        </ul>
        
      </li>
    </ul>
    <div class="btn-search" @click="changeHeight">
      <i class="ti-search search-btn"></i>
      <i class="ti-menu mobile-btn"></i>
    </div>
  </div>
</template>

<script>
export default{
  data() {
    return{
      height: "46.5px"
    }
  },
  methods: {
    changeHeight() {
      if(this.height === '46.5px') {
        this.height = "auto"
      }else{
        this.height = '46.5px'
      }
    },
    stopDefault(e) {
      e.preventDefault();
      
    }
  }
}
</script>

<style >
 #header{
   width:100%;
   background-color: var(--dark);
   position: fixed;
   top: 0;
   left: 0;
   right: 0;
   z-index: 1;
   
 }
 #nav{
   display: inline-block;
 }
 #nav > li{
   display: inline-block;
   line-height: 45px;
   text-transform: uppercase;
    position: relative;
    font-weight: 500;
 }
 #nav > li:hover{
   background: #ccc;
   cursor: pointer;
 }
 #nav > li:hover a{
    color: var(--dark);
 }
 
 #nav > li > a{
   color: var(--light);
   font-size: 15px;
   text-decoration: none;
   padding: 0 24px;
 }
 #nav .subnav{
   display: none;
   list-style: none;
    position:absolute;
    left: 0;
}
#nav > li:hover .subnav{
   display: block;
 }
#nav .subnav li{
  background-color: var(--light);
  width: 160px;
  height: 38.5px;
  padding:0 16px;
}
#nav .subnav li:hover{
  background: #ccc;
}
 #nav .subnav li a{
    color: var(--dark);
    text-decoration: none;
    line-height: 38.5px;
    text-transform: none;
 }
 .btn-search {
   font-weight: 100;
   color: var(--light);
   display: inline-block;
   float: right;
   line-height: 46.5px;
   padding: 0 24px;
   cursor: pointer;
 }
 .btn-search:hover{
   background: #f44336;
 }
 .btn-search .mobile-btn{
   display: none;
 }
</style>
