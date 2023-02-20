<script>
  import Header from './components/Header.vue';
  import Aside  from './components/Aside.vue';
  import Nav from './components/Nav.vue';
  import Main from './components/Main.vue';
  import IconBottomRight from './components/IconBottomRight.vue';
  //import Footer from './components/Footer.vue';

  export default {
      data(){
        return{
          //headerLeft
          none:true,
          block:false,
          search_position:{left:"73px"},
          best_friend_en_ligne:[{name:"Saad El Armi"}, {name:"Ñãwfal Mä NìTø"}, {name:"Reda Eskouni"},{name:"Hunter x Hunter"},{name:"Ayoub Zahir"},{name:"Taha Ahat"},{name:"Manal Ariba"},{name:"Jhon Tawr"}, {name:"Adel Homsa"}, {name:"Jhon Tawr"}, {name:"Ali eskouni"}, {name:"Andress Go"}, {name:"Malak El"},],

          //headerRight
          header_compte:true,
          header_messanger:true,
          header_menu:true,
          header_notification:true,
          header_messanger_data:[{name:"Reda",message:"Hy"},{name:"Kamal",message:"Hello"},{name:"moro",message:"صباح الخير"},{name:"Mark",message:"Hy"},{name:"Thami",message:"Hy"},{name:"Hadoum",message:"Hy"},{name:"Zaaytra",message:"Hy"},{name:"Reda",message:"Hy"},{name:"thami",message:"Hy"},{name:"Reda",message:"Hy"},{name:"Reda",message:"Hy"},{name:"Reda",message:"Hy"},{name:"Reda",message:"Hy"},{name:"Reda",message:"Hy"},{name:"Reda",message:"Hy"},{name:"Reda",message:"Hy"},{name:"Reda",message:"Hy"},{name:"Reda",message:"Hy"},{name:"Reda",message:"Hy"},]
        }
      },
      components:{
        Header, Aside, Nav, Main, IconBottomRight 
      },
      methods:{
        defaultHederRight(){
          this.header_menu = true; this.header_compte = true; this.header_messanger = true;  this.header_notification = true;
        },
        defaultHederLeft(){
          this.none = true;  this.block = false;  this.search_position.left= "73px";
        },
        returnAllToDefault(){
          this.defaultHederLeft();
          this.defaultHederRight();
        },
        //headerLeft
        search(event){
            this.defaultHederRight()
            this.none = false ;
            this.block = true ;
            this.search_position.left = "60px";
            event.stopPropagation();
        },
        arrow_back(){
            this.none = true ;
            this.block = false ;
            this.search_position.left = "73px";
        },
        //headerRight
        dropCompte(event){
          this.defaultHederLeft()
          this.header_notification = true;  this.header_menu = true;  this.header_messanger = true;
          this.header_compte = !this.header_compte;   
          event.stopPropagation()
        },
        dropMessanger(event){
          this.defaultHederLeft()
          this.header_notification = true;  this.header_menu = true;  this.header_compte = true;
          this.header_messanger = !this.header_messanger;   
          event.stopPropagation()
        }, 
        dropMenu(event){
          this.defaultHederLeft()
          this.header_notification = true;  this.header_messanger = true;  this.header_compte = true;
          this.header_menu = !this.header_menu;   
          event.stopPropagation()
        },
        dropNotification(event){
          this.defaultHederLeft()
          this.header_menu = true;  this.header_messanger = true;  this.header_compte = true
          this.header_notification = !this.header_notification;   
          event.stopPropagation()
        }
      }
  }
</script>

<template>
  <div>
    <Header 
      :returnAllToDefault="returnAllToDefault"

      :none="none"
      :block="block"
      :search_position="search_position"
      :best_friend_en_ligne="best_friend_en_ligne"
      :search="search"
      :arrow_back="arrow_back"


      :header_compte="header_compte"  :dropCompte="dropCompte"
      :header_messanger="header_messanger" :dropMessanger="dropMessanger" :header_messanger_data="header_messanger_data"  
      :header_menu="header_menu" :dropMenu="dropMenu"
      :header_notification="header_notification" :dropNotification="dropNotification"
    />
    <Aside 
      :returnAllToDefault="returnAllToDefault" 
    />
    <Nav />
    <Main />
    <IconBottomRight />
  </div>
</template>

