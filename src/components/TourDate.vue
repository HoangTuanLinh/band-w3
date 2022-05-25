<template>
    <div id="tour" class="tour">
      <div class="main">
        <h2 class="tour__heading heading">TOUR DATES</h2>
        <p class="tour__sub-heading sub-heading">Remember to book your tickets!</p>
        <div class="tour__ticket">
          <p>September <span>Sold out</span></p>
          <p>October<span>Sold out</span></p>
          <p>November <span>3</span></p>
        </div>
        <div class="list-place">

          <div class="place" v-for="(place, index) in places" :key="index">
            <img :src="`${require('@/assets/imgs/' +place.img)}`" alt="place">
            <div class="place__content">
            <h2 class="place__title"><b>{{place.title}}</b></h2>
            <p class="place__date">{{ place.date }}</p>
            <p class="place__desc">{{ place.desc }}</p>
            <button class="place__buy-btn" @click="onToggelModel">Buy Tickets</button>
            </div>
          </div>
          
        </div>
      </div>
    </div>
    <modal v-show="isOpenClose" @cancel="onToggelModel"></modal>
</template>

<script>
import modal from './modal.vue'
export default{
  data(){
    return{
      isOpenClose: false,
      places: [
        {
          img:"place1.jpg",
          title: "New York",
          date: "Fri 27 Nov 2016",
          desc: "Praesent tincidunt sed tellus ut rutrum sed vitae justo."
        },
        {
          img:"place2.jpg",
          title: "Paris",
          date: "Sat 28 Nov 2016",
          desc: "Praesent tincidunt sed tellus ut rutrum sed vitae justo."
        },
        {
          img:"place3.jpg",
          title: "San Francisco",
          date: "Sun 29 Nov 2016",
          desc: "Praesent tincidunt sed tellus ut rutrum sed vitae justo."
        },
      ]
    }
  },
  components: {
    modal
  },
  methods: {
    onToggelModel() {
      this.isOpenClose = !this.isOpenClose;
      console.log('dd')

    }
  }
}
</script>

<style scoped>
.tour{
  background: var(--dark);
  text-align: center;
  padding: 64px 0;
}
.tour__heading{
  color: var(--light);
}
.tour .tour__sub-heading{
  color: var(--light);
  margin: 15px;
}
.tour__ticket{
  background: var(--light);
  text-align: left;
  opacity: 0.8;
  margin-top: 2rem;
}
.tour__ticket p{
  padding: 0.5rem 1rem;
  border-bottom: 1px solid rgba(0, 0, 0, 0.2);
    position: relative;
}
.tour__ticket p span{
  margin-left: 1rem;
  padding:  2px 0.5rem;
  color: var(--light);
  background: #f44336;
}
.tour__ticket p:last-child span{
  background: var(--dark);
  border-radius: 50%;
  position: absolute;
  right: 20px;
}
.list-place{
  width: 100%;
  margin: 32px 0;
  display: flex;
  justify-content: space-between;
}
.list-place .place{
  width: 32%;
  
}
.list-place .place img{
  display: block;
}
.list-place .place img:hover{
  opacity: 0.6;
}
.place .place__content{
  background: var(--light);
  padding: 0 15px;
  text-align: left;
}
.place .place__content .place__title{
  font-size: 15px;
  font-weight: 500;
  padding: 15px 0;
}
.place .place__content .place__date{
  color: rgba(0, 0, 0, 0.6);
}
.place .place__content .place__desc{
  margin: 15px 0;
  line-height: 1.4;
}
.place .place__content .place__buy-btn{
  margin-bottom: 16px;
  background: var(--dark);
  color: var(--light);
  font-size: 15px;
  padding: 8px 13px;
  cursor: pointer;
  border: none;
}
.place .place__content .place__buy-btn:hover{
  background: #ccc;
  color: var(--dark);
}
</style>
