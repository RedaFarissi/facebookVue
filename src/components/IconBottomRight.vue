<script>
export default {
    data(){
        return{
            compte_hover:true,
        }
    },
    methods:{
        mouseover(){ this.compte_hover = false },
        mouseout(){ this.compte_hover = true },
    }
}
</script>

<template>
    <div style="position:fixed;bottom:13.5px;right:16px;width:67px;height:99px;" @mouseover="mouseover" @mouseout="mouseout">
      <div id="writing-mes" >
          <div class="material-icons" style="font-size:28px;color:white;">note_alt</div> 
      </div>
      <div id="holri_parent" :class="{'d-none':compte_hover ,'d-block':compte_hover==false}">
          <div id="holri">
              <div class="material-icons" style="color:white;margin-left:8px;margin-top:9px;"> more_horiz </div>
          </div>
      </div>
    </div>
</template>

<style>
  #writing-mes{
      background-color:rgba(255 255 255/11%); width:50px; height:50px; position:absolute; bottom:0px; left:16px;
      border-radius:50%; cursor:pointer; display:flex; justify-content:center; align-items:center;
  }
  #writing-mes:hover{ background-color:rgba(255 255 255/20%); }
  #holri_parent{position:absolute;right:7px;width:40px;height:40px;border-radius:50%; }
  #holri{width:40px;height:40px;border-radius:50%;background-color:rgba(255 255 255/11%);position:absolute;}
  #holri:hover{ background-color:rgba(255 255 255/20%); cursor:pointer; }
</style>