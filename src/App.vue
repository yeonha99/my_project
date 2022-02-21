<template>
  <div class="name">{{name}}</div>
  <button 
  class="btn btn-primary"
  v-on:click="updateName"
  >
  Click</button>
</template>

<script>
import {ref} from 'vue';
//숫자나 스트링 값 바꿀때 쓰는 것
import {reactive} from 'vue';
//오브젝트 값 바꿀때

export default {
  setup(){
    const name=ref('Kossie coder1')

   // const greeting = (name) =>{
   //   return 'Hello, '+name;
  //  }

    const updateName=()=>{
      name.value='Kossie Coder';
    };

      return{
       name,
       updateName
       };
  }

}
</script>

<style>
  .name{
    color:red;
  }
</style>
