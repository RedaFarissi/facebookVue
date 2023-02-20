<script>
export default{
    data(){
        return {
            clear:false
        }
    },
    props:['UsersName'],
    methods:{
        remove(event){
            this.clear = true
            event.stopPropagation();
        }
    }   
}

</script>

<template>
    <div class="cherche_amis" :class="{'d-none': clear}">
        <div class="cherche_amis_profile"> 
            <img src="../../assets/img/logo_fb.png" style="width:35px; height:35px; border-radius:50%;">
            <div style="font-size: 87%;font-weight:500;margin-left:12px"> {{ UsersName }} </div>
        </div>
        <div class="cherche_amis_clear" @click="remove">
            <div class="material-icons" style="font-size: 99%;"> clear </div>
        </div>
    </div>
</template>

<style>
.cherche_amis{ 
    display:flex; justify-content:space-between; align-items: center;cursor: pointer;
    border-radius:9px;padding:5.5px 9px;color:rgba(255 255 255/75%); 
}
.cherche_amis:hover{ background-color: rgba(255 255 255 /25%);}
.cherche_amis_profile{ display:flex; justify-content:space-between; align-items: center; }
.cherche_amis_clear{width:25px;height:25px;border-radius:50%;display:flex;justify-content:center;align-items:center; }
.cherche_amis_clear:hover{ background-color: rgba(255 255 255 /15%); }
</style>