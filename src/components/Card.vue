<template>
  <div class="rows">
      <form class="row g-3">
        <div class="col-auto">
          <label for="inputName" class="visually-hidden">Название</label>
          <input v-model="part.Name" type="text" class="form-control" id="inputName" placeholder="Название">
        </div>
          <div class="col-auto">
          <label for="inputPrace" class="visually-hidden">Цена за штуку</label>
          <input v-model="volute.Volute" type="text" class="form-control" id="inputPrace" placeholder="Цена за штуку">
        </div>  <div class="col-auto">
          <label for="inputVolute" class="visually-hidden">Кол-во</label>
          <input v-model="Prise.Praice" type="text" class="form-control" id="inputVolute" placeholder="Кол-во">
        </div>
      
        <div class="col-auto">
          <button @click="added"  class="btn btn-primary mb-3">Добавить</button>
        </div>
      </form>
      <button @click="show" class="btn btn-primary mb-3">Смотреть результат</button>
      <div class="row">
      <ul v-if="item" id="array-rendering">
        <li v-for="item in test" :key="item">
          {{ item.PName}} {{ item.PName}} {{ item.PName}}
  
      </li>
</ul>

      </div>
  </div>    
 
</template>

<script>
/* eslint-disable */
import Product from './Produckt.js'
export default {
  name: 'card',
  props:{
    msg:String
    },
    data(){
      return{
        product:[],
        part:Produckt,
        check:false,
        test:[1,2,3,4]
      }
    },
    methods:{
      added(){
        this.produc={this.part}
        alert(this.product)

      },
      show(){
        {
          this.check =true
          alert(this.product)
        }
      }
    }
  }
</script>
<style>
</style>
