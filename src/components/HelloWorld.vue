<template>
  <div id="home">
    <div class="wrapper">
      <div class="wrapper-head">
        <h1>지금의 나는<br>
        <b>얼마나 벌었을까?</b>
        </h1>
      </div>
      <div class="wrapper-body">
        <div class="month">2019.11</div>
        <div class="money">{{paycheck}}</div>
        <div class="date">2019년 11월 23일 오후 11:50</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      paycheck : 0,
    }
  },
  components: {
    'my-component': {
      template: '<div> component!!</div>'
    }
  },
  created: function(){
    
  },
  methods: {
    sum(a, b) {
      return a + b;
    },
    paycheckTimer(){
      var vm = this;
      var now = new Date();
      var paycheck = 2100000
      var millisecond = 100 * 3600 * 24 * 30;
    
      // // 월급 <- 한달 == (100 * 3600 * 24 * 30),  / 100분의 1초 
      var msPaycheck = parseFloat((paycheck / millisecond).toFixed(2))
      
      vm.paycheck = msPaycheck * 100 * 3600 * 24 * now.getDate();
       
      var playAlert = setInterval(function() {
        vm.paycheck = parseFloat(vm.paycheck) + msPaycheck;
        vm.paycheck = vm.paycheck.toFixed(2);
      }, 10);      
    }
  },
  mounted: function(){
    this.paycheckTimer();
  }


}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
#home{
  width: 100vw;
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
}
h1, h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
