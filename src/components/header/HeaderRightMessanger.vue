<script>
    import HeaderRightMessangerItem from "./HeaderRightMessangerItem.vue";                                                                                                      
    export default {
        data(){
            return{ compte_hover:true }
        },
        props:['header_messanger','dropMessanger','header_messanger_data'],
        components:{HeaderRightMessangerItem},
        methods:{
           mouseover(){ this.compte_hover = false },
           mouseout(){ this.compte_hover = true },
        }
    }
</script>

<template>
    <div>  
        <div class="haeder-right-cadre" @mouseover="mouseover" @mouseout="mouseout" @click="dropMessanger">
            <span style="color: white;font-size: 20px;" class="material-icons"> send </span>
            <div class="hrader-right-hover" :class="{'d-none':compte_hover ,'d-block':compte_hover==false}"> messanger </div>
        </div>
        <div class="cadre_for_drop_down" id="messanger" :class="{'d-none':header_messanger,'d-block':header_messanger == false}">
            <div id="messanger-header-div" class="d-flex">
                <h4  id="messanger-header-h4"> Messenger </h4>
                <div id="messanger-header-icon" class="d-flex"> 
                    <div class="messanger-header-icon-cadrs">
                        <div class="material-icons"> more_horiz </div>
                    </div>
                    <div class="messanger-header-icon-cadrs">
                        <div class="material-icons" style="transform: rotate(45deg);"> open_with </div>
                    </div>
                    <div class="messanger-header-icon-cadrs">
                        <div class="material-icons"> video_call </div>
                    </div>
                    <div class="messanger-header-icon-cadrs">
                        <div class="material-icons" style="font-size: 21px;"> drive_file_rename_outline  </div>
                    </div>
                </div>
            </div>
            <div id="input-search-messanger-cadrs" style="position: relative;">
                <input type="search" id="input-search-messanger" placeholder="Rechercher dans Messanger">
                <div class="material-icons" style="position:absolute;top:9.5px;left:9px;font-size:21px"> search </div>
            </div>
            <div class="box-messanger-amis" style="margin-top:8px;">
                <div class="box-messanger-pas-amis-div1" style="background-color:rgba(255 255 255/9%)">
                    <div class="material-icons" style="color:white;">  question_answer </div>
                </div>
                <div class="box-messanger-pas-amis-div2">
                    <span style="font-weight: 630;"> Nouvelle invitation par message</span><br>
                    <small>message</small> 
                </div>
            </div>
            <div v-for="item in header_messanger_data">
                <HeaderRightMessangerItem :name="item.name" :message="item.message" />  
            </div>
            
        </div>
    </div>
</template>

<style>
    #messanger{ height: 700px ; }
    #messanger-header-div{ display:flex;justify-content:space-between; align-items:center; height:45px; margin-left:7.5px;}
    #messanger-header-h4{color:rgba(255 255 255/85%);font-weight:750;padding-bottom:0px;margin-top:10px}
    #messanger-header-icon{display:flex;justify-content:space-around;align-items:center;width:48%;margin-left:8px;margin-top:4px;}
    .messanger-header-icon-cadrs{width:30px;height:30px;border-radius:50%;display:flex;justify-content:center;align-items:center;}
    .messanger-header-icon-cadrs:hover{ background-color: rgba(255 255 255/15%); cursor: pointer;}
    #input-search-messanger-cadrs{ width:96%; height:37.5px; margin-left:2%; margin-top:6px; border-radius:28px; }
    #input-search-messanger{width:100%;height:100%;outline:none;border:none;border-radius:29px;background-color:#3a3b3c; }
    #input-search-messanger::placeholder{padding-left:36px;font-size:92%;padding-bottom:9px;font-weight:450;}
    .box-messanger-amis{width:100%;height:70px;display:flex;align-items:center;}
    .box-messanger-amis:hover{ background-color:rgba(255 255 255/4.5%); cursor:pointer; border-radius:9px;}
    .box-messanger-pas-amis-div1{ width:55.5px; height:55.5px; border-radius:50%; margin-left:6px; }
    .box-messanger-pas-amis-div1 div{width:100%;height:100%;display:flex;justify-content:center;align-items:center;font-size:25px;}
    .box-messanger-pas-amis-div2{ font-size:90%; overflow:hidden; margin-left:10px; }
</style>