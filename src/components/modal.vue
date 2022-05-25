<template>
  <div class="model " @click.self="onClose">
        <div class="model-container ">
            <div class="model-close" @click="onClose">
                <i class="ti-close"></i>
            </div>
            <header class="model-header">
                <i class="model-heading-icon ti-bag"></i>
                Tickets
            </header>
            <form action="">
            <div class="model-body">
                <lable for="quantity" class="moddel-lable">
                    <i class="ti-shopping-cart"></i>
                    Tickets, $15 per person
                </lable>
                <input id="quantity" type="text" class="model-input" placeholder="How many?" required>

                <lable class="moddel-lable">
                    <i class="ti-user"></i>
                    Send To
                </lable>
                <input type="email" class="model-input" placeholder="Enter email?" required>

                <button type="submit" id="buy-ticket">
                    Pay <i class="ti-check"></i>
                </button>
            </div>
            </form>

            <footer class="model-footer">
                <p class="model-help">Need <a href="">help?</a></p>
            </footer>
        </div>
    </div>
</template>
<script>
export default{
  data() {
    return{

    }
  },
  methods: {
    onClose() {
      this.$emit('cancel')
    }
  }
  
}
</script>
<style scoped>
  .model{
    position: fixed;
    top: 0;
    right: 0;
    left: 0;
    bottom: 0;
    background-color: rgba(0, 0, 0, 0.4);
    display: flex;
    align-items: center;
    justify-content: center;
    z-index: 2;
}
.model.open{
    display: flex;
}
.model-container {
    background: #fff;
    width: 900px;
    max-width: calc(100% - 32px);
    min-height: 200px;
    position: relative;
    animation: modelFadeIn ease 0.5s;
}
.model-close {
    position: absolute;
    right: 0;
    top: 0;
    color: #fff;
    padding: 12px;
    cursor: pointer;
    opacity: 0.8;
}
.model-close:hover {
    opacity: 1;
}
.model-header {
    background: #009688;
    height: 129px;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 30px;
    letter-spacing: 4px;
    color: #fff;
}
.model-heading-icon{
    margin-right: 16px;
}
.model-body {
    padding: 16px;
}
.model-input {
    width: 100%;
    border: 1px solid #ccc;
    font-size: 15px;
    padding: 10px;
    margin-bottom: 24px;   
}
.moddel-lable {
    margin-bottom: 12px;
}
#buy-ticket {
    width: 100%;
    padding: 18px;
    color: #fff;
    background: #009688;
    border: none;
    text-transform: uppercase;
    font-size: 15px;
    cursor: pointer;
}
#buy-ticket:hover {
    background: #ccc;
    color: #000;
}
.model-footer{
    font-size: 15px;
    padding: 12px;
    text-align: right;
}
.model-footer a{
    color: #2196F3;
}
@keyframes modelFadeIn {
    from{
        opacity: 0;
        transform: translateY(-140px);
    }
    to{
        opacity: 1;
        transform: translateY(0);
    }
}
</style>
