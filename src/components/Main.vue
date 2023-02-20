<script setup> </script>

<template>
<main id="main"> 
        <div id="main_story">  
            <div style="cursor: pointer; ">  
                <img src="../assets/img/profile.jpg" id="add_story_profile">  
                <div id="Creer_une_story">
                    <div id="style_add_circle_gray">
                        <div id="circle_white">
                            <div class="material-icons"> add_circle </div>
                        </div> 
                    </div>
                    <p>Creer une <br> story</p>
                </div> 
            </div>
            <div class="story-user-child"> 
                <div class="story-profile-user">
                    <img src="../assets/img/logo_fb.png" style="width:100%; height:100%; object-fit:cover;border-radius:50%">
                </div>
                <img src="../assets/img/profile.jpg" class="story-profile"> 
            </div>
            <div  class="story-user-child"> 
                <div class="story-profile-user">
                    <img src="../assets/img/logo_fb.png" style="width:100%; height:100%; object-fit:cover;border-radius:50%">
                </div>
                 <img src="../assets/img/profile.jpg" class="story-profile">   
             </div>
            <div  class="story-user-child"> 
                <div class="story-profile-user">
                    <img src="../assets/img/logo_fb.png" style="width:100%; height:100%; object-fit:cover;border-radius:50%">
                </div>
                 <img src="../assets/img/logo_fb.png" class="story-profile">   
             </div>
            <div  class="story-user-child"> 
                <div class="story-profile-user">
                    <img src="../assets/img/logo_fb.png" style="width:100%; height:100%; object-fit:cover;border-radius:50%">
                </div>
                 <img src="../assets/img/logo_fb.png" class="story-profile">   
             </div>
            <div  class="story-user-child"> 
                <div class="story-profile-user">
                    <img src="../assets/img/logo_fb.png" style="width:100%; height:100%; object-fit:cover;border-radius:50%">
                </div>
                 <img src="../assets/img/logo_fb.png" class="story-profile">   
             </div>
        </div>
        <div id="creer_une_publication">
            <div class="creer_une_publication_div1 flex-around-center-style">
                <img src="../assets/img/profile.jpg">
                <input type="text" placeholder="Quoi de neuf , Reda?" >
            </div>
            <hr style="color:gray;width:95%;margin:9px auto">
            <div class="creer_une_publication_div1 flex-around-center-style">
                <div class="flex-around-center-style hover" style="margin-left: 15px;">
                    <div class="material-icons" style="color:rgb(243 66 95);font-size:30px;"> videocam </div>
                    <div class="ktaba"> Video en direct </div>
                </div>
                <div class="flex-around-center-style hover">
                    <div class="material-icons" style="color:rgb(69 189 98);font-size:30px;"> crop_original </div>
                    <div  class="ktaba"> Photo/video </div>
                </div>
                <div class="flex-around-center-style hover" style="margin-right: 15px;" id="Humeur">
                    <div class="material-icons" style="color:rgb(247 185 40);font-size:30px;"> tag_faces </div>
                    <div class="ktaba"> Humeur/Activite </div>
                </div>
            </div>
        </div>

        <div id="creer_selon">
            <div id="creer_selon_div1" onclick="creer_salon.creer_salon()">               
                <div class="material-icons" style="font-size:30px;margin-right:5px"> video_call </div>
                <div style="font-size: 76%;"> Creer un selon </div>
            </div>
            <div id="creer_selon_div2">
                <div class="material-icons" > arrow_forward_ios </div>
                <div class="creer_selon_div2_div"><img src="../assets/img/logo_fb.png" class="creer_selon_div2_img" style="margin-left: 0px;"> </div> 
                <div class="creer_selon_div2_div"><img src="../assets/img/logo_fb.png" class="creer_selon_div2_img"></div>
                <div class="creer_selon_div2_div"><img src="../assets/img/logo_fb.png" class="creer_selon_div2_img"></div>
                <div class="creer_selon_div2_div"><img src="../assets/img/logo_fb.png" class="creer_selon_div2_img"></div>
                <div class="creer_selon_div2_div"><img src="../assets/img/logo_fb.png" class="creer_selon_div2_img"></div>
                <div class="creer_selon_div2_div"><img src="../assets/img/logo_fb.png" class="creer_selon_div2_img"></div>
                <div class="creer_selon_div2_div"><img src="../assets/img/logo_fb.png" class="creer_selon_div2_img"></div>
                <div class="creer_selon_div2_div"><img src="../assets/img/logo_fb.png" class="creer_selon_div2_img"></div>
                <div class="creer_selon_div2_div"><img src="../assets/img/logo_fb.png" class="creer_selon_div2_img"></div>
                <div class="creer_selon_div2_div"><img src="../assets/img/logo_fb.png" class="creer_selon_div2_img"></div>
                <div class="creer_selon_div2_div"><img src="../assets/img/logo_fb.png" class="creer_selon_div2_img"></div>
                <div class="creer_selon_div2_div"><img src="../assets/img/logo_fb.png" class="creer_selon_div2_img"></div>
                <div class="creer_selon_div2_div"><img src="../assets/img/logo_fb.png" class="creer_selon_div2_img"></div>
                <div class="creer_selon_div2_div"><img src="../assets/img/logo_fb.png" class="creer_selon_div2_img"></div>
                <div class="creer_selon_div2_div"><img src="../assets/img/logo_fb.png" class="creer_selon_div2_img"></div>
            </div>
        </div>
        <section class="section_staut_with_img">
            <div class="main-head-post">
                <div class="main-head-post-part1"> 
                    <img src="../assets/img/logo_fb.png" class="main-head-post-part1-img">
                    <div class="main-head-post-part1-div"> User Name</div>
                </div>
                <div class="main-head-post-part2">
                    <span class="material-icons" style="color:rgba(255 255 255 /75%)"> more_horiz </span>
                </div>
            </div>
            <div class="statut">
                statut . Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptates asperiores enim amet necessitatibus, omnis odio, suscipit rem ratione quis nihil veniam in laboriosam eius! Sapiente vel corporis vitae omnis ipsum!Lorem ipsum, dolor sit amet consectetur adipisicing elit. Cum, saepe itaque optio quo praesentium veniam eveniet eos nostrum alias animi aliquam quia aspernatur. Sint nemo, quas ipsum debitis mollitia magnam!Lorem ipsum dolor sit amet consectetur adipisicing elit. Velit illo, eius perferendis recusandae veritatis debitis reprehenderit ex hic expedita id nihil illum officia maiores et quas beatae nobis nam quasi.
            </div>
            <div class="section_images">
                <img src="../assets/img/logo_fb.png">
            </div>
            <div class="section_vue">
                <span class="material-icons section_vue_part1" style="font-size:95%;background-color:#2e89ff;padding:4.8px;border-radius:50%;cursor:pointer;"> thumb_up </span>
                <div class="section_vue_part2"> <span>0</span> commentairs </div>
            </div>
            <hr style="width:90%; margin-left:5%;margin-top:-2px;margin-bottom:7px; color:rgba(255 255 255/75%);">
            <div class="comonter_up">
                <div class="comonter_up_shild">
                    <div class="material-icons">thumb_up</div>
                    <div style="margin-left:7px;"> J'aime </div>
                </div>
                <div class="comonter_up_shild">
                    <div class="material-icons">mode_comment</div> 
                    <div  style="margin-left:7px;">Commenter</div>
                </div>
                <div class="comonter_up_shild">
                    <div class="material-icons">reply</div> 
                    <div  style="margin-left:7px;">Partager</div>
                </div>
            </div>
        </section>
        
        <section id="connaissez-vous">
            <div class="main-head-post">
                <div class="main-head-post-part1"> 
                    <div class="main-head-post-part1-div" style="font-size:100%; font-weight:550"> Connaissez-vous...</div>
                </div>
                <div class="main-head-post-part2">
                    <span class="material-icons" style="color:rgba(255 255 255 /75%)"> more_horiz </span>
                </div>  
            </div>
            <div id ="scro">
                <div id="connaissez-vous-ajouter">
                
                </div>
            </div>
        </section>
    </main>
</template>

<style scoped>
#main{ width:45.9%; height:200vh; margin-left:27%; margin-top:57px; padding-top:24px; }
#main_story{ display:flex; justify-content:space-between; height:190px; margin-bottom:20px; }
#main_story > div{ background-color:#242526; height:100%; border-radius:9px; width:15.7%; } 
#add_story_profile{ width:100%; height:60%; border-radius:9px 9px 0px 0px; }
#Creer_une_story{ position:relative; }
#style_add_circle_gray{ 
    position:absolute; top:-19px; left:35%; color:#2e89ff; background-color:#242526; width:39px; height:39px; border-radius:50%;
}
#circle_white{ 
  background-color:white;width:20px;height:20px;border-radius: 50%;
    transform: translate(48% ,50%);display:flex; align-items:center;justify-content:center;}
#style_add_circle_gray .material-icons{ font-size:38px; }
#Creer_une_story>p{ color:white; padding-top:21px; text-align:center; font-size:12px; }
.story-profile{ width:100%; height:100%; border-radius:9px; object-fit:cover; }
.story-user-child{ position: relative; cursor: pointer; }
.story-profile-user{ 
    position:absolute;top:7%;left:9%;width:40px;height:40px;background-color:orangered;border-radius:50%;border:4px solid #2e89ff;
}
/*********************************************** */
#creer_une_publication{width:100%; height:125px; background-color:#242526; border-radius:9px; padding-top:9px; }
.creer_une_publication_div1{ height:45px; margin:auto; }
.creer_une_publication_div1 img{ width:39px; height:39px; background-color:red; border-radius:50%;}
.creer_une_publication_div1 input{
    width:calc(100% - 40px); height:40px; background-color:#3a3b3c;margin-left: 9px;
    outline:none; border:none; border-radius:35px; padding-left:12px; color:seashell;
}
.flex-around-center-style{display:flex; justify-content:space-between; align-items:center; padding:3px 20px; border-radius:9px;}
.hover:hover{ background-color:#3a3b3c; cursor:pointer; } 
.ktaba{ color:rgba(255 255 255/70%); padding-left:6px; font-size:87%;font-weight: 500;}
/*********************************************** */
#creer_selon{
    display: flex;align-items: center;padding-left: 20px;
    width: 100%; height: 65px; background-color: #242526; margin-top: 17px; border-radius: 9px;
}
#creer_selon_div1{
    display: flex; justify-content: center; align-items: center; color: white;cursor: pointer;
    width:150px; height:38px; border-radius:45px; border:1.5px solid #263951; float:left;
}
#creer_selon_div1:hover{ background-color: rgba(255 255 255/5%);}
#creer_selon_div2{  width:calc(100% - 170px); height:38px; float:left; margin-left: 20px; overflow: hidden;position: relative; }
#creer_selon_div2 [class="material-icons"] {
   position:absolute; right:1.5%; top: 4px; width:30px; height:30px; background-color: #3e4042; border-radius: 50%; 
   color: seashell; font-size: 20px; text-align: center; line-height: 28px;cursor: pointer;
}
.creer_selon_div2_div{ width:38px; height:38px; border-radius: 50%;float: left; margin-left: 11px; position: relative;}
.creer_selon_div2_div::before{
    content:"";width:11.5px;height:11.5px;border-radius:50%;background-color:#242526;position:absolute; right:0%;bottom:0%; 
}
.creer_selon_div2_div::after{
    content:"";width:6.5px;height:6.5px;border-radius:50%;background-color:#31a24c;position:absolute;right:3px;bottom:3px; 
}
.creer_selon_div2_img{ width:100%; height:100%; border-radius:50%;}
.creer_selon_div2_img:hover{ background-color:rgba(255 255 255/5%); }
/*********************************************** */
.menu-list{width:196px; height:470px; box-shadow:none; position:fixed; right:33px; top:102px; border-radius:9px;}
/*********************************************** */
.section_staut_with_img{
    width:100%; background-color:#242526; border-radius:9px; margin-top:19px; padding-top:14px; padding-bottom:3px;
}
.main-head-post{height:45px;display:flex;justify-content:space-between;align-items:center; cursor:pointer; }
.main-head-post-part1{ margin-left:13px; display:flex; align-items:center; }
.main-head-post-part1-img{ width:40px; height:40px; border-radius:50%; margin-right:10px; }
.main-head-post-part1-div{ font-size:92%; font-weight:600;color:rgba(255 255 255/75%); }
.main-head-post-part2{ 
  margin-right:13px;width:35px;height:35px;border-radius:50%;display:flex;justify-content:center;align-items: center;font-size:95%;
}
.main-head-post-part2:hover{ background-color: rgba(255 255 255/25%);}
.statut{ min-height:50px; max-height: 70px; overflow: hidden; color:rgba(255 255 255/75%); margin:19px;}
.section_images{ width: 100%;height:590px; border:0.02px solid gray; }
.section_images img{width: 100%; max-height: 100%; object-fit: cover; cursor:pointer;}
.section_vue{display:flex; justify-content:space-between; align-items:center; color:rgba(255 255 255/75%); height:45px;}
.section_vue_part1{ margin-left:15px; display:flex; align-items:center;}
.section_vue_part1 div{ margin-left:15px; display:flex; align-items:center;}
.section_vue_part2{margin-right:15px; font-size: 90%;}
.comonter_up{ display:flex; justify-content:center; align-items:center; }
.comonter_up_shild{width:30%;display:flex;justify-content:center;align-items:center;padding:10px 0px;color:rgba(255 255 255 /75%) }
.comonter_up_shild [class="material-icons"]{ color:transparent; -webkit-text-stroke: 1px rgba(255 255 255/75%) ;}
.comonter_up_shild:hover{ background-color: rgba(255 255 255/25%); width:30%;cursor: pointer;border-radius: 9px; }
/********************************************** */
#connaissez-vous{height:436px; background-color:#242526; border-radius:9px; margin-top:19px; padding-top:14px; width:100%;}
#scro{width: 100%;height:328px;overflow-y:hidden;overflow-x:auto;}
#scro::-webkit-scrollbar{width:0px;}
#connaissez-vous-ajouter{width:320%;height:310px;padding-left:15px;overflow-y:hidden;overflow-x:auto;}
.connaissez-vous-ajouter-carde{border:0.4px solid gray;border-radius:9px;width:200px;margin-right:9px;height:310px;float:left;}
.connaissez-vous-ajouter-carde-img{ height:65%; cursor:pointer;}
.connaissez-vous-ajouter-carde-img:hover{ height:65%; cursor:pointer; opacity:0.85;}
.connaissez-vous-ajouter-carde-img img{width:100%;height:100%;border-radius:9px 9px 0px 0px; border-bottom:0.09px solid gray;}
.connaissez-vous-ajouter-carde-name{height:11%;color:rgba(255 255 255/85%);padding-top:5px;padding-left:10px;font-weight:560;}
.connaissez-vous-ajouter-carde-add{ display:flex;justify-content:center;align-items:flex-end;height:24%;border-radius:0px 0px 9px 9px;}
.connaissez-vous-ajouter-carde-button{
    display:flex; justify-content:center; align-items:flex-end; margin-bottom:14.5px; width:80%;
    color:rgb(45 136 255);background-color:rgb(38 57 81); padding:5px 0px; border-radius:9px; cursor:pointer;
}
.connaissez-vous-ajouter-carde-button:hover{background-color: rgba(38 57 81/70%);}
#connaissez-vous button{
    width:calc(100% - 34px);color:rgba(255 255 255/75%);outline:none;border:none;border-radius:9px;margin-left:17px;
    padding: 7.5px 0px;background-color:#242526;margin-top:12px ; clear: both;margin-top:-5px;}
#connaissez-vous button:hover{
    background-color: rgba(255 255 255/5%);
}


/**************************** salon ******************/

#salon{position:fixed;top:calc(59% - 250px);right:calc(50% - 250px);opacity:1;cursor:pointer;width:502px;
    height:340px;background-color:rgb(36 37 38);border-radius:6px;box-shadow:4px 5px 12px rgba(0 0 0/30%)}
.sellon_header{width:37px;height:37px;border-radius:50%;background-color:rgba(255 255 255/8%);color:white;
   display:flex;justify-content:center;align-items:center;margin-right:5px;color:rgba(255 255 255/75%)}
#salon_cadr{display:flex;justify-content:center;align-items:center;width:80px;height:80px;margin-top:-45px;
    border-radius:50%;border:1.2px solid rgb(37 47 60);position:absolute;right:calc(51% - 46.5px);}
#salon_cadr span{ font-size:40px; color:white; }
#salon >p{margin-top:37px;color:white;font-weight:700;font-size:20px;text-align:center;}
.salon-cadr-div{padding:5.5px 12px;border-radius:8px;display:flex;align-items:center;}
.salon-cadr-div:hover{background-color:rgba(255 255 255/9%);}
#salon button{margin-top:9px;border:none;outline:none;border-radius:5px;width:97%;margin-left:1.5%;
    height:36.5px;font-weight:500;background-color:rgb(35 116 225);color:rgba(255 255 255/85%)}
#salon button:hover{ background-color:rgb(35 116 225/85%) }

@media only screen and ( max-width:1200px ){
    #main { width:66.9%; margin-left:1%; }  
}

@media only screen and ( max-width:945px ){
    #main { width:90%; margin-left:5%; }   
}
@media only screen and ( max-width:709px ){
    #main { width:99%; margin-left:0.5%; }   
}
@media only screen and ( max-width:500px ){
    #Humeur{ display: none;}
}
</style>