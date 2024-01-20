<template>
  <div class="hello">
    <div class="card" style="width: 18rem;">
      <img src="https://i.playground.ru/p/jjQzDaTny6cQ_zPrNu7sPA.png" class="card-img-top" alt="...">
       <div class="card-body">
        <p class="card-text">{{msg}}</p>
        <p class="card-text">{{descr}}</p>
      
      </div>
      <button v-on:click:"renove" type="button" class="btn btn-danger">Делит</button>

    </div>
  </div>
</template>

<script>
/*eslint-disable*/
export default {
  name: 'Card',
  props: {
     msg: String,
    descr: String,
   foto: String
  },
  methods:{ 
    renove(){
      alert('Ликвидировали!!')
    }
  }
}
</script>
<style>
</style>
