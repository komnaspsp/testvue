<template>
  <div class="rows">
    <slot></slot>
      <div class="row g-3">
        <div class="col-auto">
          <label for="inputName" class="visually-hidden">Название</label>
          <input v-model="part.PName" type="text" class="form-control" id="inputName" placeholder="Название">
        </div>
          <div class="col-auto">
          <label for="inputPrace" class="visually-hidden">Цена за штуку</label>
          <input v-model="part.pVolute" type="text" class="form-control" id="inputPrace" placeholder="Цена за штуку">
        </div>  
        <div class="col-auto">
          <label for="inputVolute" class="visually-hidden">Кол-во</label>
          <input v-model="part.Praise" type="text" class="form-control" id="inputVolute" placeholder="Кол-во">
        </div>
      
        <div class="col-auto">
          <button @click="added"  class="btn btn-primary mb-3">Добавить</button>
        </div>
      </div>
      <button @click="show" class="btn btn-primary mb-3">Смотреть результат</button>
      <div class="row">
      <ul v-if="check" id="array-rendering">
        <li v-for="item in product" :key="item">
          {{ item.PName}} {{ item.Praise}} {{ item.pVolute}}
  
      </li>
</ul>
      </div>
  </div>    
  <div class="alert alert-secondary" role="alert">
      у нас в корзине лежит :{{resultSumm}} количество товара
</div>

    <slot></slot>
</template>

<script>
/* eslint-disable */
import Product from './Product.js'
export default {
  name: 'card',
  props:{
    msg:String
    },
    data(){
      return{
        product:[],
        part:Product,
        check:false,
      
      }
    },
    methods:{
      added(){
        this.product.push({...this.part});
      },
      show(){
        
          this.check =!this.check
      }
      },
       computed:{
        resultSumm(){
        return this.product.length;
          }
       }
       }
</script>
<style>
*{
  background: Aquamarine

}
</style>
