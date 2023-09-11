<script>
   import NavItem from './nav/NavItem.vue';
   
   export default{
       data(){
           return{
               en_ligne_contact:[
                   {name:"Fname Lname"},
                   {name:"Fname Lname"},
                   {name:"Fname Lname"},
                   {name:"Fname Lname"},
                   {name:"Fname Lname"},
                   {name:"Fname Lname"},
                   {name:"Fname Lname"},
                   {name:"Fname Lname"},
                   {name:"Fname Lname"},
                   {name:"Fname Lname"},
                   {name:"Fname Lname"},
                   {name:"Fname Lname"},
                   {name:"Fname Lname"},
                   {name:"Fname Lname"},
                   {name:"Fname Lname"},
                   {name:"Fname Lname"},
                   {name:"Fname Lname"},
                   {name:"Fname Lname"},
                   {name:"Fname Lname"},
               ]
           }
       },
       props:['sendMessageBox'],
       components:{ NavItem  },
   }
</script>

<template>
    
    <nav id="nav" @click="returnAllToDefault">  
        <p class="Sponsorise"> Sponsorisé </p> 
        <div class="sponsorise1">
            <div class="sponsorise1_img"> 
                <img src="../assets/img/jeux.jpg">
            </div>
            <div class="sponsorise1_p">
                <p style="color:rgba(255 255 255/82%); padding-top:14px;" > Title number 1 </p>
                <p style="color:rgba(255 255 255/80%); font-size:70%; margin-top:-5px;"> exemple.com </p>
            </div>
        </div>
        <div class="sponsorise1 mt-1">
            <div class="sponsorise1_img"> 
                <img src="../assets/img/logo_fb.png">
            </div>
            <div class="sponsorise1_p">
                <p style="color:rgba(255 255 255/82%); padding-top:14px; "> Title number 2 </p>
                <p style="color:rgba(255 255 255/80%); font-size:70%; margin-top:-5px;"> exemple.com </p>
            </div>
        </div>
        <hr style="color:snow;">
        <div class="Contact-ktaba">
            <div style="font-weight:600;font-size:95%;"> Contacts</div>
            <div style="margin-right:5%;">
                <div class="material-icons" style="margin-left:3px;cursor:pointer;"> search </div>
                <div class="material-icons" style="margin-left:3px;cursor:pointer;"> more_horiz </div>
            </div>
        </div>        
        <div id="NAV" v-for="item in en_ligne_contact">
            <NavItem :name="item.name" :sendMessageBox="sendMessageBox" />
        </div>
    </nav>

</template>

<style scoped>
#nav{width:23.8% ;height:100vh;position:fixed;right:0%;top:57px;overflow-x:hidden;overflow-y:auto; }
nav::-webkit-scrollbar { width:8px; }
nav::-webkit-scrollbar-track {  border-radius:5px; box-shadow:white; visibility:hidden; }
nav:hover::-webkit-scrollbar-track { visibility:visible; } 
nav::-webkit-scrollbar-thumb { border-radius:5px; background-color:gray; visibility:hidden; }
nav:hover::-webkit-scrollbar-thumb { visibility:visible; }
.Sponsorise { margin:20px 0px; font-size:105%; color:rgba(255 255 255/85%);}
.sponsorise1{ width:100%; height:90px; border-radius:9px; cursor:pointer; }
.sponsorise1:hover{ background-color:#242526; }
.sponsorise1_img{ float:left; width:46%; height:80px; margin-top:5px; padding:0px 5px;}
.sponsorise1_img img{ width:100%; height:100%; object-fit:cover; border-radius:9px; }
.sponsorise1_p{ width:51%; float:left; padding-left:20px;}
.Contact-ktaba{display:flex;justify-content:space-between;color:rgba(255 255 255/75%)}
/*********************************************** */
.bouge{margin-bottom:2px;margin-left:-6px;padding-left:7px;padding-top:4.5px;padding-bottom:4.5px;}
/*********************************************** */
.content-nav{ 
    display:flex;align-items:center;padding:6.5px 7px; overflow-y:auto; cursor:pointer;width:90%;border-radius:9px;
}
.content-nav:hover{ background-color: rgba(255 255 255 / 15%); }
.content-nav-users{ width:33px; height:33px; border-radius:50%; margin-right:15px; position:relative;}
.content-nav-users::before{
    content: ""; width:11.5px; height:11.5px; border-radius:50%; background-color:#18191a; position:absolute; 
    right:0%; bottom: 0%; 
}
.content-nav-users::after{
    content: ""; width:6.5px; height:6.5px; border-radius:50%; background-color:#31a24c;
    position:absolute; right:3px; bottom:3px; 
}
.users_name{ color:rgba(255 255 255 / 75%);}

@media only screen and ( max-width:1200px ){
    #nav{width: 28.8%;}
}
@media only screen and ( max-width:945px ){
    #nav{display: none !important;  }    
}
</style>