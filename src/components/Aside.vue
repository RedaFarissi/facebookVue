<script>
    import AsideItem from './aside/AsideItem.vue'
    export default{
        data(){
            return{
                items:[{icon:"people_alt",name:"Amis"},{icon:"groups",name:"Groups"},{icon:"storefront",name:"Groups"},{icon:"ondemand_video",name:"Watch"},{icon:"update",name:"Souvenirs"},{icon:"bookmark",name:"Enregistements"},{icon:"keyboard_arrow_down",name:"Voir plus"}]
            }
        },
        props:['returnAllToDefault'],
        components:{AsideItem}
    }
    
</script> 

<template>
  <aside id="aside" @click="returnAllToDefault">
    <a class="content-aside">
        <div class="material-icons" style="font-size:40px;margin-right:9px">account_circle</div>
        <div id="user_name" style="font-weight: 520;"> Reda Eskouni </div>
    </a>
    <div v-for="item in items">
        <AsideItem :icon="item.icon" :name="item.name" />
    </div>
    
    <div style="width: 95%; height:0.5px; background-color:gray;margin:12px auto"></div>
    <p> Vos raccourcis </p>
    <div class="content-aside bouge">
        <div class="content-aside-style-gaming">
            <img src="../assets/img/logo_fb.png">
        </div>
        <div id="user_name" style="font-weight:520;">  Raccourcis Name </div>
    </div>
    <div class="content-aside bouge">
        <div class="content-aside-style-gaming">
            <img src="../assets/img/ball.jpg">
        </div>
        <div id="user_name" style="font-weight:520;"> 8 Ball Pool </div>
    </div>
    <div class="content-aside bouge">
        <div class="content-aside-style-gaming">
            <img src="../assets/img/candy.jpg">
        </div>
        <div id="user_name" style="font-weight:520;"> Candy Crash Saga </div>
    </div>
    <div class="content-aside bouge">
        <div class="content-aside-style-gaming">
            <img src="../assets/img/devlopment.jpg">
        </div>
        <div id="user_name" style="font-weight:520;"> Developpement Informatique maroc </div>
    </div>
  </aside>
</template>

<style>
    #aside{
        width:23%; height:calc(100vh - 57px); padding:21px 14.5px; color:rgba(245 245 245 /85%);
        position:fixed; bottom: 0px; margin-right: 45px; overflow-x: hidden; overflow-y: auto;   
    }
    .content-aside{
        display:flex; align-items:center; margin-bottom:2px; overflow-y:auto; padding:3px 0px; 
        cursor:pointer; color:aliceblue;text-decoration: none;
    }
    .content-aside:hover{ background-color: #3a3b3c; border-radius: 9px;}
    .content-aside-style{width: 41px;height:39px; text-align:center; display:flex; align-items:center;margin-left: 5px;}
    .icons-tags{ font-size:27px; margin-right:9px }
    .content-aside-style-gaming{ 
        width: 41px;height:39px; text-align:center; display:flex; 
        align-items:center;margin-right: 9px; 
    }
    .content-aside-style-gaming img {width: 100%; height: 100%; border-radius: 9px; margin-right: 15px;}

    @media only screen and ( max-width:1200px ){
        #aside { display:none; }
    }
</style>