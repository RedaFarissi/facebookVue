<script>
    import MainItem from './main/MainItem.vue';
  
    export default{
        data(){
            return{
                like_mouseover:false,
            }
        },
        components:{
            MainItem
        }
    }
</script>

<template>
<main id="main" @click="returnAllToDefault"> 
        <div id="main_story">  
            <div style="cursor: pointer; ">  
                <img src="../assets/img/logo_fb.png" id="add_story_profile">  
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
      
        <MainItem />
        <MainItem />
        <MainItem />
        <MainItem />
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


/**************************** salon ******************/
/* 
#salon{
    position:fixed;top:calc(59% - 250px);right:calc(50% - 250px);opacity:1;cursor:pointer;width:502px;
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
#salon button:hover{ background-color:rgb(35 116 225/85%) } */


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