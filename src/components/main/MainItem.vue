<script>
    export default{
        data(){
            return{
                like_mouseover:false,
            }
        },
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
                <span class="material-icons section_vue_part1" style="font-size:95%;background-color:#2e89ff;padding:4.8px;border-radius:50%;cursor:pointer;"> thumb_up </span>
                <div class="section_vue_part2"> <span>0</span> commentairs </div>
            </div>
            <hr style="width:90%; margin-left:5%;margin-top:-2px;margin-bottom:7px; color:rgba(255 255 255/75%);">
            <div class="comonter_up position-relative">
                <div @mouseover="like_mouseover=true" @mouseout="like_mouseover=false" class="comonter_up_shild commenter_like">
                    <div class="material-icons">thumb_up</div>
                    <div style="margin-left:7px;"> J'aime </div>
                </div>
                <div  v-if="like_mouseover"  class="commenter_emoji d-flex justify-content-around align-items-center p-1 position-absolute"> 
                    <div class="d-flex justify-content-center align-items-center bg-primary rounded-circle p-2">
                        <i class="fs-5 fa-solid text-white fa-thumbs-up"></i>
                    </div>
                    <div class="bg-danger d-flex justify-content-center align-items-center rounded-circle p-2">
                        <i class="fs-5 fa-solid text-white fa-heart"></i>
                    </div>
                    <i class="fs-3 fa-solid fa-face-grin text-warning"></i>
                    <i class="fs-3 fa-solid fa-face-surprise text-warning"></i>
                    <i class="fs-3 fa-solid fa-face-sad-tear text-warning"></i>
                    <i class="fs-3 fa-solid fa-face-angry text-danger"></i>
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
</template>


<style>
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


.commenter_emoji{ 
    width: 300px; left:50px; top:-52px; border-radius: 40px; background-color: white;
}
</style>