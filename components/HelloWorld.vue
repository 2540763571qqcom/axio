<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
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
  created(){
    // this.$axios.get("http://www.wwtliu.com/sxtstu/blueberrypai/getChengpininDetail.php")
    // .then(res=>{
    //   console.log(res)
    // })
    // .catch(error =>{
    //   console.log(error)
    // })
    let url = this.Host + "/awos/getNewAwos"
    this.$axios.get(url,{
      param:{
        count: 10,
        start: 0
      }
    })
    .then(res =>{
      console.log(res.data)
    })
    .catch(error => {
      console.log(error)
    })
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
