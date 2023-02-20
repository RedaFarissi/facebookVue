<script>
export default {
    data(){
        return{
            compte_hover:true
        }
    },
    props:['header_compte','dropCompte'],
    methods:{
        mouseover(){ this.compte_hover = false },
        mouseout(){ this.compte_hover = true },
    }
}
</script>
<template>
    <div id="allCompte">
        <div class="haeder-right-cadre" @mouseover="mouseover" @mouseout="mouseout" @click="dropCompte">
            <span class="material-icons" style="color:white; font-size:20px;" id="arrow_drop_down">arrow_drop_down</span>
            <div class="hrader-right-hover" :class="{'d-none':compte_hover ,'d-block':compte_hover==false}"  id="compte_hidden"> Compte </div>
        </div>
        <div class="cadre_for_drop_down" id="compte" :class="{'d-none':header_compte,'d-block':header_compte == false}">
            <div id="compte-first-child" style="display:flex;">
                <div id="profile">
                    <img src="../../assets/img/logo_fb.png" class="haeder-left-logo">
                </div>
                <div style="margin-left:2px;color:rgba(255 255 255/75%)"> 
                    <div style="font-weight:660;margin-left:9px"> User Name </div>
                    <div style="font-size:88%;margin-left:9px"> Voir votre profil </div>
                </div>
            </div>
            <hr style="color:rgba(255 255 255/75%); width:95%; margin-left:2.5%;margin-top:8px;margin-bottom:8px">
            <div class="votre_avis">
                <div class="votre_avis_icon">
                    <div class="material-icons" style="font-size:20px;color:white"> announcement </div>
                </div>
                <div style="margin-left:13px;color:rgba(255 255 255/75%)">
                    <div style="font-weight:629;font-size:94%;">Donner votre avis</div>
                    <div style="font-size:78%;">Aidez-nous a ameliorer Facebook</div>
                </div>
            </div>
            <hr style="color:rgba(255 255 255/75%); width:95%; margin-left:2.5%;margin-top:8px;margin-bottom:8px">
            <div class="votre_avis">
                <div class="votre_avis_icon">
                    <div class="material-icons" style="font-size:22px;color:white"> settings </div>
                </div>                    
                <div style="margin-left:13px;color:rgba(255 255 255/75%);font-weight:629;"> Paramètres et confidentialité </div>
                <div class="material-icons" style="color:rgba(255 255 255/80%);position:absolute;right:15px"> arrow_forward_ios </div>
            </div>
            <div class="votre_avis">
                <div class="votre_avis_icon">
                    <div class="material-icons" style="font-size:22px;color:white"> help </div>
                </div>                    
                <div style="margin-left:13px;color:rgba(255 255 255/75%);font-weight:629;"> Aide et assistance </div>
                <div class="material-icons" style="color:rgba(255 255 255/80%);position:absolute;right:15px"> arrow_forward_ios </div>
            </div>
            <div class="votre_avis">
                <div class="votre_avis_icon">
                    <div class="material-icons" style="font-size:24px;color:white;transform:rotate(-12deg);margin-left:-1px"> nightlight_round </div>
                </div>                    
                <div style="margin-left:13px;color:rgba(255 255 255/75%);font-weight:629;"> Affichage et accessibilite </div>
                <div class="material-icons" style="color:rgba(255 255 255/80%);position:absolute;right:15px"> arrow_forward_ios </div>
            </div>
            <div class="votre_avis">
                <div class="votre_avis_icon">
                    <div class="material-icons" style="font-size:24px;color:white;"> logout </div>
                </div>                    
                <div style="margin-left:13px;color:rgba(255 255 255/75%);font-weight:629;"> Se déconnecter </div>
            </div>
            <p style="color:rgba(255 255 255/45%);font-size:69%;margin:2px 9px;"> Confidentialité  · Conditions générales  · Publicités  · Choix publicitaires   · Cookies . Plus  · Meta © 2022</p>
        </div>
    </div>
</template>

<style>
#compte-first-child {display:flex; align-items:center; height:70px; border-radius:9px; }
#compte-first-child:hover { background-color:rgba(255 255 255/15%); }
#profile{width:50px;height:50px; border-radius:50%; margin:9px; margin-top: 2px; }
#profile img{width:60px; height:60px; border-radius:50%; }
.votre_avis{display:flex; align-items:center; height:48px; border-radius:8px; padding-left:7px; cursor:pointer;} 
.votre_avis:hover{background-color: rgba(255 255 255/15%);} 
.votre_avis_icon{
    display:flex;justify-content:center;align-items:center;color:rgba(255 255 255/80%);
    width:36.5px;height:36.5px;background-color:rgba(255 255 255/11%);border-radius:50%;
}
</style>