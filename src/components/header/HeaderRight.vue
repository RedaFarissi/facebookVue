<script>
    import HeaderRightProfile from './HeaderRightProfile.vue'
    import HeaderRightMessanger from './HeaderRightMessanger.vue'
    import HeaderRightMenu from './HeaderRightMenu.vue'
    import HeaderRightNotification from './HeaderRightNotification.vue'
    import HeaderRightCompte from './HeaderRightCompte.vue';

    export default {
        data(){},
        props:[
            'header_compte','dropCompte',
            'header_messanger','dropMessanger','header_messanger_data',
            'header_menu','dropMenu',
            'header_notification','dropNotification'
        ],
        components:{
            HeaderRightProfile,HeaderRightMessanger,HeaderRightMenu,HeaderRightNotification,HeaderRightCompte
        },
        methods:{

        }
    }


</script>
<template>
    <div class="haeder-right">
        <HeaderRightProfile />
        <HeaderRightMenu 
            :header_menu="header_menu"
            :dropMenu="dropMenu"
        />
        <HeaderRightMessanger 
            :header_messanger="header_messanger" 
            :dropMessanger="dropMessanger"
            :header_messanger_data="header_messanger_data"
        />
        <HeaderRightNotification 
            :header_notification="header_notification"
            :dropNotification="dropNotification"
        />
        <HeaderRightCompte 
            :header_compte="header_compte" 
            :dropCompte="dropCompte"
        />
    </div>
</template>

<style>
.cadre_for_drop_down{ 
    position:absolute; top:57px; right:16px ;width:360px; height:400px; background-color:greenyellow; 
    border-radius:9px;background-color:#242526; padding:9px; color:rgba(255 255 255/75%); 
    overflow-y: auto;box-shadow:2px 2px 10px rgba(0 0 0 /35%);
}
.cadre_for_drop_down::-webkit-scrollbar { width:8px; }
.cadre_for_drop_down::-webkit-scrollbar-track { border-radius:5px; box-shadow:white; visibility:hidden; }
.cadre_for_drop_down:hover::-webkit-scrollbar-track{ visibility: visible; }
.cadre_for_drop_down::-webkit-scrollbar-thumb{border-radius:5px; background-color:gray; visibility:hidden;}
.cadre_for_drop_down:hover::-webkit-scrollbar-thumb{ visibility:visible; }
.haeder-right{ width:13.5%; display:flex; justify-content:space-around; margin-right: 20px;}
.hrader-right-hover {
    position: absolute;bottom:-36px; background-color:rgba(255 255 255 / 70%); 
    width:max-content;  border-radius: 9px;font-size:75%; padding:4.5px 9px; 
    font-weight: 400; box-shadow: 1px 1px 3px rgba(0 0 0 /5%); z-index: 999;
}
.haeder-right-cadre{
    background-color: #3a3b3c; width:40px; height:40px;margin:0px 2px;cursor: pointer;
    border-radius:40px;display: flex; justify-content:center;align-items: center;
}
.haeder-right-cadre:hover{ background-color: rgba(255 255 255 /35%); }

@media only screen and ( max-width:945px ){
    .haeder-right{width: 17%;}
}

@media only screen and ( max-width:709px ){
    .haeder-right{width: 23%;}
}

</style>