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
        <div class="money">203000</div>
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
      msg: 'Welcome to Your Vue.js App'
    }
  },
  components: {
    'my-component': {
      template: '<div> component!!</div>'
    }
  },
  created: function(){
    
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
