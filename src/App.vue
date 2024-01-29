<template>
<input class="field1" type="text" v-model="userName" placeholder="Имя">
<input class="field2" type="password" v-model="userPass" placeholder="Пароль">
<input class="field3" type="email" v-model="userEmail" placeholder="Email">
<p className="error">{{error}}</p>
<button @click="sendData()">Отправить</button>
<div v-if="users.length == 0">
У нас нет пользователей
</div>
<div v-else-if="users.length == 1">
User has 1 element
</div>
<div v-else>
User has more than 1 element
</div>

<div v-for="(el,index) in users" :key="index">
<h2>{{el.name}}</h2>
<p>{{el.email}}-<b>{{el.pass}}</b></p>
<p></p>
</div>

</template>


<script>
/* eslint-disable */ 
export default{
  data(){
    return{
      users:[],
      error:'',
      userName:'',
      userPass:'',
      userEmail:''
           }
    },
  methods:{
    sendData(){
      if(this.userName ==''){
        this.error='Имя не выбрано';
        return;
      }else if (this.userPass == ''){
        this.error='Пароль не выбран';
        return;
      }else if(this.userEmail == ''){
        this.error='Email не выбран';
        return;
      }
      this.error=""
      this.users.push({
        name:this.userName,
        pass:this.userPass,
        email:this.userEmail
      })

    }
   
    }

}
  
</script>


<style scoped>
.field1,.field2,.field3{
  background-color: #fff;
  border-color: #bdbdbd;
   outline: 0;
  box-shadow: 0 0 0 0.2rem rgba(158, 158, 158, 0.25);
  

}


</style>
