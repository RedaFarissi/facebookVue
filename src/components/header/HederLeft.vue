<script>
    import HeaderLeftItem from './HeaderLeftItem.vue'
    export default{
        data(){   },
        props:['none','block','search_position','best_friend_en_ligne','search','arrow_back'],
        components:{ HeaderLeftItem },
       
    }
</script>

<template>
    <div class="haeder_left">
        <div id="haeder-left-part-1">
            <div id="arrow_back_icon_parent_div" @click="arrow_back" :class="{'d-none':none,'d-block':block}">
                <div class="material-icons" id="arrow_back_icon"> keyboard_backspace </div>
            </div>
            <div class="material-icons" id="search_icon" :style="search_position">search</div>
            <img src="../../assets/img/logo_fb.png" :class="{'d-none':block,'d-block':none}" class="haeder-left-logo">
            <input type="search" @click="search" name="search" class="haeder-left-search" placeholder="Rechercher sur Facebook">
        </div>
        
        <div id="haeder-left-part-2" :class="{'d-none':none,'d-block':block}">
            <div class="part2_div_first">  
                <p style="font-size: 98%;font-weight:600"> Recherches récentes </p>
                <p style="font-size: 85%;color:#2e89ff">Modifier</p>
             </div>
            <div v-for="i in best_friend_en_ligne">
                <HeaderLeftItem :UsersName="i.name"  />
            </div>
        
        </div>
    </div>
</template>

<style>

.haeder_left{ width:20.5%;  background-color:#242526; align-self:start; }
#haeder-left-part-1{ display:flex;align-items:center; padding-left:15px; margin-top:8px; }
#arrow_back_icon_parent_div{ width:34px; height:32px; ; border-radius:50%;}
#arrow_back_icon_parent_div:hover{ background-color:rgba(255 255 255 /15%);cursor:pointer;  }
#arrow_back_icon{ color: rgba(255 255 255/75%); font-size:24px; line-height:32px; margin-left:4px; } 
#search_icon{ position:absolute; /*left:73px;*/ color:rgba(255 255 255/65%); font-size:22px; }
.haeder-left-logo{ width:40px; height:40px; border-radius:40px; }
.haeder-left-search{ 
    width:100%; height:40px; border-radius:44px; border:none; outline:none; margin-left:8px;
    background-color:#3a3b3c; color:rgba(255 255 255 /75%); padding-left:20px; padding-bottom:3px; 
    display: block;
}
::placeholder{padding-left:9px;color: rgba(255 255 255 /50%); font-size:17px;}
.haeder-left-search::placeholder{padding-left:17px; color:rgba(255 255 255 /60%); font-size:14.5px;}
a{ text-decoration:none; color:rgba(255 255 255); }
a:hover{ color:rgba(255 255 255); }
/*********************************************** */
#haeder-left-part-2{ max-height: 500px; padding-top:57px; padding-bottom: 9px; overflow: hidden;}
.part2_div_first{
    display:flex;justify-content:space-between;align-items:center;
    color:rgba(255 255 255/75%); padding: 0px 9px;
}
@media only screen and ( max-width:1370px ){
    .haeder-left-search { display: none; }    
    #search_icon { margin-left:-9px; padding:9px; border-radius:50%; background-color:#3a3b3c; cursor:pointer; }
}
@media only screen and ( max-width:1200px ){
    .haeder-left{width:20%}
}
@media only screen and ( max-width:945px ){
    .haeder-left{width:34%}
}
</style>