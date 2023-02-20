<script >
import HederLeft from './header/HederLeft.vue';
import HeaderMiddle from './header/HeaderMiddle.vue';
import HederRight from './header/HeaderRight.vue';

export default {
  data(){},
  components:{
    HederLeft,
    HeaderMiddle,
    HederRight
  },
  props:[
      'returnAllToDefault',
      //hederLeft
      'none','block','search_position','best_friend_en_ligne','search','arrow_back',
      //hederRight
      'header_compte','dropCompte',
      'header_messanger','dropMessanger','header_messanger_data',
      'header_menu','dropMenu',
      'header_notification','dropNotification'
  ]
}
</script>

<template>
    <header id="header" @click="returnAllToDefault">
        <HederLeft 
          :none="none"
          :block="block"
          :search_position="search_position"
          :best_friend_en_ligne="best_friend_en_ligne"
          :search="search"
          :arrow_back="arrow_back"
        />
        <HeaderMiddle />
        <HederRight 
          :header_compte="header_compte" 
          :dropCompte="dropCompte" 

          :header_messanger="header_messanger" 
          :dropMessanger="dropMessanger"
          :header_messanger_data="header_messanger_data"

          :header_menu="header_menu"
          :dropMenu="dropMenu"

          :header_notification="header_notification"
          :dropNotification="dropNotification"
        />
    </header>
</template>

<style scoped>
  header{
      position:fixed; display:flex; justify-content:space-between; background-color:#242526; align-items:center; 
      height:56px; top:0%; width:100%; z-index:850; border-bottom:0.3px solid rgba(90 90 90/75%);
  }
</style>