<script>
    export default {
        data(){
            return{
                compte_hover:true
            }
        },
        props:['header_menu','dropMenu'],
        methods:{
           mouseover(){ this.compte_hover = false },
           mouseout(){ this.compte_hover = true },
        }
    }

</script>
<template>
    <div>
        <div class="haeder-right-cadre" @mouseover="mouseover" @mouseout="mouseout" @click="dropMenu">
            <span style="color: white;font-size: 25px;" class="material-icons">apps</span>
            <div class="hrader-right-hover" :class="{'d-none':compte_hover ,'d-block':compte_hover==false}"> menu </div> 
        </div>
        <div  class="cadre_for_drop_down" id="menu" :class="{'d-none':header_menu,'d-block':header_menu == false}">
            <h4>Menu</h4>
            <div class="cadre_for_drop_down" style="height:max-content;box-shadow:none;left:16px;top:52px;overflow:hidden">
                <div style="position:relative;">
                    <div class="material-icons" style="position:absolute;left:14px;top:15px;font-size:20px;color:rgba(255 255 255/65%)"> search </div>
                    <input type="search" id="search_menu" placeholder="Rechercher dans le menu">
                </div>
                <div style="font-size:16px;font-weight:500;color:white;margin-top:7px;margin-left:8px">Social</div>
                <div class="menu-cadrs" style="margin-top:5px;">
                    <div class="material-icons" style="font-size:30px;margin-top:9px;margin-left:12px"> important_devices </div>
                    <div style="font-size:85%;margin-left:15px;">
                        <span style="color:rgba(255 255 255);font-size:13px;font-weight:550;"> Événements </span><br>
                        <small style="font-weight:450;line-height:-90%;">
                            <div style="margin-top:-3px;">Trouver des activités et des evenements auxquels </div>
                            <div style="margin-top:-3px;">vous pouvez participes en ligne ou en personne  </div>
                            <div style="margin-top:-3px;">pres de chez vous, ou organisez-en.</div>
                        </small> 
                    </div>
                </div>
                <div class="menu-cadrs">
                    <div class="material-icons" style="font-size:30px;margin-top:9px;margin-left:12px"> group </div>
                    <div style="font-size:85%;margin-left:15px;">
                        <span style="color:rgba(255 255 255);font-size:15px;font-weight:550;"> Amis </span><br>
                        <small style="font-weight:450;line-height:-90%;">
                            <div style="margin-top:-3px;"> Trouver des activités ou des personnes  </div>
                            <div style="margin-top:-3px;"> connaissez. </div>
                        </small>
                    </div>
                </div>
                <div class="menu-cadrs">
                    <div class="material-icons" style="font-size:30px;margin-top:9px;margin-left:12px"> groups </div>  
                    <div style="font-size:85%;margin-left:15px;">
                        <span style="color:rgba(255 255 255);font-size:15px;font-weight:550;"> Groups </span><br>
                        <small style="font-weight:450;line-height:-90%;">
                            <div style="margin-top:-3px;"> Entrez en contact avec des personnes qui partagent   </div>
                            <div style="margin-top:-3px;"> vos centeres d'interet. </div>
                        </small>
                    </div>
                </div>
                <div class="menu-cadrs">
                    <div class="material-icons" style="font-size:30px;margin-top:9px;margin-left:12px"> padding </div>  
                    <div style="font-size:85%;margin-left:15px;">
                        <span style="color:rgba(255 255 255);font-size:15px;font-weight:550;"> Fil d'actualite </span><br>
                        <small style="font-weight:450;line-height:-90%;">
                            <div style="margin-top:-3px;"> Consultez des publications pertinentes mises en </div>
                            <div style="margin-top:-3px;"> ligne par des personnes et des Pages que vous  </div>
                            <div style="margin-top:-3px;"> suivez. </div>
                        </small>
                    </div>
                </div>
                <div class="menu-cadrs" style="padding: 3px 1px;">
                    <div class="material-icons" style="font-size:30px;margin-top:9px;margin-left:12px"> outlined_flag </div>  
                    <div style="font-size:85%;margin-left:15px;">
                        <span style="color:rgba(255 255 255);font-size:15px;font-weight:550;">Page </span><br>
                        <small style="font-weight:450;line-height:-90%;">
                            <div style="margin-top:-3px;"> Decouvrez des entreprises et entrez en contact avec  </div>
                            <div style="margin-top:-3px;"> elles sur Facebook.   </div>
                        </small>
                    </div>
                </div>
                <hr style="margin-top:15px; margin-bottom:15px; width:95%;margin-left:2.5%; ">
                <div style="font-size:16px;font-weight:500;color:white;margin-top:-5px;margin-left:8px"> Divertissement </div>
                <div class="menu-cadrs" style="padding: 3px 1px;margin-top:4px">
                    <div class="material-icons" style="font-size:30px;margin-top:9px;margin-left:12px"> extension </div>  
                    <div style="font-size:85%;margin-left:15px;">
                        <span style="color:rgba(255 255 255);font-size:15px;font-weight:550;">Videos de jeux </span><br>
                        <small style="font-weight:450;line-height:-90%;">
                            <div style="margin-top:-3px;"> Regardez des parties et suivez les streamers que   </div>
                            <div style="margin-top:-3px;"> vous aimez.   </div>
                        </small>
                    </div>
                </div>
                <div class="menu-cadrs" style="padding: 3px  1px;">
                    <div class="material-icons" style="font-size:30px;margin-top:5px;margin-left:12px"> videogame_asset </div>  
                    <div style="font-size:85%;margin-left:15px;padding: 3px  0px;">
                        <div style="color:rgba(255 255 255);font-size:15px;font-weight:550;"> Jouer a des jeux</div>
                        <small style="font-weight:450;line-height:-90%;">
                            <div style="margin-top:-3px;"> Jouez a vos jeux favoris. </div>
                        </small>
                    </div>
                </div>
                <div class="menu-cadrs" style="padding: 3px 1px;">
                    <div class="material-icons" style="font-size:30px;margin-top:9px;margin-left:12px"> ondemand_video </div>  
                    <div style="font-size:85%;margin-left:15px;">
                        <span style="color:rgba(255 255 255);font-size:15px;font-weight:550;"> Watch  </span><br>
                        <small style="font-weight:450;line-height:-90%;">
                            <div style="margin-top:-3px;"> Decouvrez des suggestions de video bases sur vos  </div>
                            <div style="margin-top:-3px;"> centers d'interet et vos contacts.   </div>
                        </small>
                    </div>
                </div>
                <hr style="margin-top: 15px;width:95%;margin-left:2.5%;margin-bottom: 15px;">
                <div style="font-size:16px;font-weight:500;color:white;margin-top:-5px;margin-left:8px"> Shopping </div>
                <div class="menu-cadrs" style="margin-top:5px;">
                    <div class="material-icons" style="font-size:30px;margin-top:9px;margin-left:12px;transform:rotate(-45deg)"> credit_card </div>
                    <div style="font-size:85%;margin-left:15px;">
                        <span style="color:rgba(255 255 255);font-size:15px;font-weight:550;"> Facebook Pay </span><br>
                        <small style="font-weight:450;line-height:-90%;">
                            <div style="margin-top:-3px;">Profitez d'un moyen simple et securise pour </div>
                            <div style="margin-top:-3px;">effectuer des paiements sur les applications que </div>
                            <div style="margin-top:-3px;">vous utilisez deja.</div>
                        </small>
                    </div>
                </div>
                <div class="menu-cadrs" style="padding:3px  1px;">
                    <div class="material-icons" style="font-size:30px;margin-top:5px;margin-left:12px"> storefront </div>  
                    <div style="font-size:85%;margin-left:15px;padding:3px  0px;">
                        <div style="color:rgba(255 255 255);font-size:15px;font-weight:550;"> Marketplace</div>
                        <small style="font-weight:450;line-height:-90%;">
                            <div style="margin-top:-3px;"> Achetez et vendez autour de vous. </div>
                        </small>
                    </div>
                </div>
                <hr style="margin-top: 15px;width:95%;margin-left:2.5%;margin-bottom: 15px;">
                <div style="font-size:16px;font-weight:500;color:white;margin-top:-5px;margin-left:8px"> Personnel </div>
                <div class="menu-cadrs" style="padding: 3px 1px;">
                    <div class="material-icons" style="font-size:30px;margin-top:9px;margin-left:12px"> inventory_2 </div>  
                    <div style="font-size:85%;margin-left:15px;">
                        <span style="color:rgba(255 255 255);font-size:15px;font-weight:550;"> Activite publicitarire recente  </span><br>
                        <small style="font-weight:450;line-height:-90%;">
                            <div style="margin-top:-3px;"> Retrouvez toutrs les annonces avec lesquelles vous </div>
                            <div style="margin-top:-3px;"> avec interagi sur Facebook .   </div>
                        </small>
                    </div>
                </div>
            </div>
            <div class="cadre_for_drop_down menu-list ms-5">
                <div style="font-size:20px;font-weight:660;padding-left:2px;margin-top:-1.5px;">Créer</div>    
                <div class="menu-cadrs" style="padding:6px 0px;margin-top:15px;color:white;display:flex;align-items:center;"> 
                    <div style="margin-right:10px;margin-left:7px;width:36px;height:36px;background-color:rgba(255 255 255/20%);border-radius:50%;display:flex;align-items:center;justify-content:center;">
                        <div class="material-icons" style="font-size:22px;color:white;"> edit_note </div>
                    </div>
                    <div style="font-size:85%;font-weight:600;"> Publication </div>
                </div>
                <div class="menu-cadrs" style="padding:6px 0px;color:white;display:flex;align-items:center;"> 
                    <div style="margin-right:10px;margin-left:7px;width:36px;height:36px;background-color:rgba(255 255 255/20%);border-radius:50%;display:flex;align-items:center;justify-content:center;">
                        <div class="material-icons" style="font-size:22px;color:white;"> auto_stories </div>
                    </div>
                    <div style="font-size:85%;font-weight:600;"> Story </div>
                </div>
                <div class="menu-cadrs" style="padding:6px 0px;color:white;display:flex;align-items:center;"> 
                    <div style="margin-right:10px;margin-left:7px;width:36px;height:36px;background-color:rgba(255 255 255/20%);border-radius:50%;display:flex;align-items:center;justify-content:center;">
                        <div class="material-icons" style="font-size:22px;color:white;"> video_call </div>
                    </div>
                    <div style="font-size:85%;font-weight:600;"> Salon </div>
                </div>
                <hr style="margin-top: 9px;width:90%; margin-left:5%;">
                <div class="menu-cadrs" style="padding:6px 0px;color:white;display:flex;align-items:center;margin-top:-8px"> 
                    <div style="margin-right:10px;margin-left:7px;width:36px;height:36px;background-color:rgba(255 255 255/20%);border-radius:50%;display:flex;align-items:center;justify-content:center;">
                        <div class="material-icons" style="font-size:22px;color:white;">  outlined_flag  </div>
                    </div>
                    <div style="font-size:85%;font-weight:600;"> Page </div>
                </div>
                <div class="menu-cadrs" style="padding:6px 0px;color:white;display:flex;align-items:center;"> 
                    <div style="margin-right:10px;margin-left:7px;width:36px;height:36px;background-color:rgba(255 255 255/20%);border-radius:50%;display:flex;align-items:center;justify-content:center;">
                        <div class="material-icons" style="font-size:22px;color:white;">  volume_mute  </div>
                    </div>
                    <div style="font-size:85%;font-weight:600;"> Publicite </div>
                </div>
                <div class="menu-cadrs" style="padding:6px 0px;color:white;display:flex;align-items:center;"> 
                    <div style="margin-right:10px;margin-left:7px;width:36px;height:36px;background-color:rgba(255 255 255/20%);border-radius:50%;display:flex;align-items:center;justify-content:center;">
                        <div class="material-icons" style="font-size:20px;color:white;border:2px solid white;border-radius:50%;">  groups  </div>
                    </div>
                    <div style="font-size:85%;font-weight:600;"> Groupe </div>
                </div>
                <div class="menu-cadrs" style="padding:6px 0px;color:white;display:flex;align-items:center;"> 
                    <div style="margin-right:10px;margin-left:7px;width:36px;height:36px;background-color:rgba(255 255 255/20%);border-radius:50%;display:flex;align-items:center;justify-content:center;">
                        <div class="material-icons" style="font-size:20px;color:white;">  add_to_photos  </div>
                    </div>
                    <div style="font-size:85%;font-weight:600;"> Evenement </div>
                </div>
                <div class="menu-cadrs" style="padding:6px 0px;color:white;display:flex;align-items:center;"> 
                    <div style="margin-right:10px;margin-left:7px;width:36px;height:36px;background-color:rgba(255 255 255/20%);border-radius:50%;display:flex;align-items:center;justify-content:center;">
                        <div class="material-icons" style="font-size:20px;color:white;"> shopping_bag </div>
                    </div>
                    <div style="font-size:85%;font-weight:600;"> Petite annonce <br>Maketplace </div>
                </div>
            </div>
        </div>
    </div>
</template>

<style>
    #menu{ 
        height:calc(98.5vh - 55px);margin-top:-4px;width:608px;background-color:#323436;
        color:rgba(255 255 255/50%); z-index: 999; width:750px;
    }
    #menu h4{ 
        width:582px; position:fixed; z-index:950; background-color:#323436; color:rgba(255 255 255/85%); 
        font-weight:700; margin-top:-9px; margin-left:7px; padding-top:12px; padding-bottom: 10px;
    }
    #search_menu{
        width:98%; height:36px; margin:6px 1%; border-radius:33px; outline:none; border:none; 
        background-color:rgb(58 59 60);padding-bottom:4px; color:rgba(255 255 255/80%)
    }
    #search_menu::placeholder{ font-size:95%; padding-left:35px; margin-top:-20px; }
    .menu-cadrs{  display:flex; padding:2px 1px; border-radius:8px; cursor:pointer; }
    .menu-cadrs:hover{ background-color:rgba(255 255 255 / 12%); }

</style>