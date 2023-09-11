<script>

    
    

    export default{
        data(){
            return{
                like_mouseover:false,
                like_mouseout:true,

                add_like : false ,
                add_heart: false ,
                add_smil: false ,
                add_surprise: false ,
                add_sad: false ,
                add_angry : false,
            }
        },
        methods:{
            hundleEmoji(like=false,heart=false,smil=false,surprise=false,sad=false,angry=false){
                this.add_like = like ;
                this.add_heart = heart ;
                this.add_smil = smil ;
                this.add_surprise = surprise ;
                this.add_sad = sad ;
                this.add_angry = angry;
            },
            addLike(){ 
                this.add_like = !this.add_like; 
                this.hundleEmoji(this.add_like)
            },
            addHeart(){ 
                this.add_heart = !this.add_heart;  
                this.hundleEmoji(false,this.add_heart)
            },
            addSmil(){     
                this.add_smil = !this.add_smil; 
                this.hundleEmoji(false,false,this.add_smil)
            },
            addSurprise(){ 
                this.add_surprise = !this.add_surprise; 
                this.hundleEmoji(false,false,false,this.add_surprise) 
            },
            addSad(){ 
                this.add_sad = !this.add_sad;
                this.hundleEmoji(false,false,false,false,this.add_sad)
            },
            addAngry(){ 
                this.add_angry = !this.add_angry; 
                this.hundleEmoji(false,false,false,false,false,this.add_angry)
            },
        }
    }
</script>

<template>
    <section class="section_staut_with_img">
        <div class="main-head-post">
            <div class="main-head-post-part1"> 
                <img src="../../assets/img/logo_fb.png" class="main-head-post-part1-img">
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
            <img src="../../assets/img/logo_fb.png">
        </div>
        <div class="section_vue">
            <div class="d-flex align-items-center ps-2">
                0<span class="material-icons section_vue_part1" style="font-size:95%;background-color:#2e89ff;padding:4.8px;border-radius:50%;cursor:pointer;"> thumb_up </span>
            </div>
            <div class="section_vue_part2"> <span>0</span> commentairs </div>
        </div>
        <hr style="width:90%; margin-left:5%;margin-top:-2px;margin-bottom:7px; color:rgba(255 255 255/75%);">
        <div class="comonter_up position-relative">
            <!-- handle Like and j'adore and other emoji  -->
            <div @mouseover="like_mouseover=true;like_mouseout=flase" @mouseout="like_mouseover=false;like_mouseout=true" class="comonter_up_shild commenter_like">
                <div v-if="add_like" class="d-flex">
                    <div class="d-flex justify-content-center align-items-center cursor-pointer bg-primary rounded-circle p-2 me-2">
                        <i class="fs-6 fa-solid text-white fa-thumbs-up"></i> 
                    </div> 
                    <div class="mt-1 text-primary">J'aime </div>
                </div>
                <div v-else-if="add_heart" class="d-flex">
                    <div class="bg-danger d-flex justify-content-center align-items-center cursor-pointer rounded-circle p-2 me-2">
                        <i class="fs-6 fa-solid text-white fa-heart"></i>
                    </div>
                    <div class="mt-1 text-danger">J'adore </div>
                </div>
                <div v-else-if="add_smil" class="d-flex">
                    <i  class="fs-3 fa-solid fa-face-grin text-warning cursor-pointer me-2"></i>
                    <div class="mt-1 text-warning">Haha </div>
                </div>
                <div v-else-if="add_surprise" class="d-flex">
                    <i class="fs-3 fa-solid fa-face-surprise text-warning cursor-pointer me-2"></i>
                    <div class="mt-1 text-warning">Wouah</div>
                </div>
                <div v-else-if="add_sad" class="d-flex">
                    <i @click="add_sad = true" class="fs-3 fa-solid fa-face-sad-tear text-warning cursor-pointer me-2"></i>
                    <div class="mt-1 text-warning">Triste</div>
                </div>
                <div v-else-if="add_angry" class="d-flex">
                    <i @click="add_angry = true" class="fs-3 fa-solid fa-face-angry text-danger cursor-pointer me-2"></i>
                    <div class="mt-1 text-danger">On colere</div>
                </div>
                <div v-else  class="d-flex justify-content-between"> 
                    <div class="material-icons me-3">thumb_up</div>
                    J'aime 
                </div>
            </div>
            <div :class="{'d-block':like_mouseover,'d-none':like_mouseout}" @mouseover="like_mouseover=true;like_mouseout=flase" @mouseout="like_mouseover=false;like_mouseout=true" class="commenter_emoji position-absolute pb-3">
                <div  class="d-flex justify-content-around align-items-center p-1 bg-light"> 
                    <div @click="addLike" class="d-flex justify-content-center align-items-center cursor-pointer bg-primary rounded-circle p-2">
                        <i class="fs-6 fa-solid text-white fa-thumbs-up"></i>
                    </div>
                    <div @click="addHeart" class="bg-danger d-flex justify-content-center align-items-center cursor-pointer rounded-circle p-2">
                        <i class="fs-6 fa-solid text-white fa-heart"></i>
                    </div>
                    <i @click="addSmil" class="fs-3 fa-solid fa-face-grin text-warning cursor-pointer"></i>
                    <i @click="addSurprise" class="fs-3 fa-solid fa-face-surprise text-warning cursor-pointer"></i>
                    <i @click="addSad" class="fs-3 fa-solid fa-face-sad-tear text-warning cursor-pointer"></i>
                    <i @click="addAngry" class="fs-3 fa-solid fa-face-angry text-danger cursor-pointer"></i>
                </div>
            </div>
            <!-- handle comment -->
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
</template>


<style>
.cursor-pointer{ cursor: pointer;}

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


.commenter_emoji{ width: 300px; left:50px; top:-42px; }
.commenter_emoji>div{ border-radius: 40px;}
</style>