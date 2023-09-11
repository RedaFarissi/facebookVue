<script>
    export default{
        data(){

        },
        props:['name','sendMessageBox']
    }
</script>

<template>
  <div @click="sendMessageBox" class="div-en-ligne d-flex align-items-center p-1  rounded ps-1" style="cursor:pointer;">
     <div class="img-en-ligne position-relative">
         <img class="w-100 rounded-circle" src="../../assets/img/logo_fb.png"/>
         <div class="en-ligne rounded-circle">
            <div class="rounded-circle"> </div>
         </div>
     </div>
     <b class="ms-3 text-light">{{ name }}</b>
  </div>
</template>

<style>
    .div-en-ligne:hover{ background-color: rgba(255 255 255 /13%);}
    .img-en-ligne{ width:47px; height:47px; }
    .en-ligne{ 
        width:12px; height:12px; position:absolute; 
        bottom:3px; right:3px; background-color: #18191a;
        display: flex; justify-content: center; align-items: center;
    }
    .en-ligne>div{
        width:8px; height:8px; background-color: #31a24c;
    }
</style>