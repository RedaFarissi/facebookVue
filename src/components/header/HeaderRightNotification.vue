<script>
   import HeaderRightNotificationItem from './HeaderRightNotificationItem.vue';
   
    export default {
        data(){
            return{
                compte_hover:true
            }
        },
        props:['header_notification','dropNotification'],
        components:{HeaderRightNotificationItem},
        methods:{
           mouseover(){ this.compte_hover = false },
           mouseout(){ this.compte_hover = true },
        }
    }
</script>

<template>
    <div>
        <div class="haeder-right-cadre" @mouseover="mouseover" @mouseout="mouseout" @click="dropNotification">
            <span style="color: white;font-size: 20px;" class="material-icons">notifications</span>
            <div class="hrader-right-hover" :class="{'d-none':compte_hover ,'d-block':compte_hover==false}"> notifications </div>
        </div>
        <div class="cadre_for_drop_down" id="notification" :class="{'d-none':header_notification,'d-block':header_notification == false}">
            <div style="display:flex; justify-content:space-between; align-items:center;height:45px;margin-left:7.5px"> 
                <h4 style="color:rgba(255 255 255/85%);font-weight:750;padding-bottom:0px;"> Notifications </h4>
                <div class="cadrsquare">
                    <div class="material-icons"> more_horiz </div>
                </div>
            </div>
            <div class="notification_style_P">
                <div class="notification_style_T"> Tout</div>
                <div  class="notification_style_N"> Non lu</div>
            </div>
            <div class="hadra_notification_P">
                <div class="hadra_notification">Plus tôt</div>
                <div class="hadra_notification2">Voir tout</div>
            </div>
            <HeaderRightNotificationItem />
        </div>
    </div>
</template>

<style>
    #notification{ height:calc(98.5vh - 55px);margin-top: -4px; }
  .notification_style_P{display:flex;align-items:center;margin-left:2px;height:45px;margin-top:-9px}
  .notification_style_T{margin-left:5.5px;border-radius:39px;background-color:rgb(38 57 81);padding:7px 12px;
      font-size:90%;font-weight:550;color:rgb(44 129 239) }
  .notification_style_N{ margin-left:8px; background-color:rgba(255 255 255/11%); color:rgba(255 255 255/90%);
      border-radius:39px;padding:7px 12px;font-size:90%;font-weight:550; }
  .hadra_notification_P{display:flex;justify-content:space-between;align-items:center;height:32px;}
  .hadra_notification{font-weight:600; margin-left:8px; color:rgba(255 255 255/90%);}
  .hadra_notification2{ font-size:86%; color:#4599ff; letter-spacing:0.2px; margin-right:5px; }
  .notification_box{ height:72px; border-radius:9px; padding:2px; display:flex;}
  .notification_box:hover{ background-color: rgba(255 255 255/15%);cursor:pointer;}
  .notification_box_menu{ 
      width:56px;height:56px;background-color:red;border-radius:50%;position:relative;
      margin-left:5px;margin-top:2px; 
  }
  .notification_box_menu_icon{
      display:flex; justify-content:center; align-items:center;
      position:absolute;bottom:-5px;right:-7px;width:27px;height:27px;border-radius:50%;
  }

    .cadrsquare{display:flex;justify-content:center;align-items:center;height:39px;width:39px;border-radius:50%;}
    .cadrsquare:hover{ background-color: rgba(255 255 255/15%); cursor:pointer;}
</style>