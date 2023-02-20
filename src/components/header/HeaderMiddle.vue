<script>
</script>

<template>
        <div class="haeder-middle">
            <div> 
                <span class="material-icons haeder-middle-logo" style="font-size:30px;color:transparent;-webkit-text-stroke:1px rgba(255 255 255 /75%);">home</span>  
            </div>
            <div> 
                <span class="material-icons haeder-middle-logo">ondemand_video</span>  
            </div>
            <div> 
                <span class="material-icons haeder-middle-logo">storefront</span>   
            </div>
            <div> 
                <span class="material-icons haeder-middle-logo" style="border-radius:50%;border:1px solid rgba(255 255 255 /75%);padding:1px;font-size:22px;">groups</span>  
            </div>
            <div> 
                <span class="material-icons haeder-middle-logo" id="haeder-middle-right1">view_quilt</span>  
               
            </div>
        </div>
</template>

<style scoped>
.haeder-middle{width:45%; height:40px; display:flex; justify-content:space-around; margin-top:-8px;margin-left:-12px;}
.haeder-middle div{padding:24px 55px; display:flex; justify-content:center; align-items: center; border-radius: 9px;}
.haeder-middle div:hover{ cursor: pointer; background-color:rgba(255 255 255/9%); }
.haeder-middle-logo{font-size:173%; color:rgba(255 255 255 /65%); margin-top: 3px;}
#haeder-middle-right2{display: none;}

@media only screen and ( max-width:1200px ){
    #haeder-middle-right1{ display:none; }
    #haeder-middle-right2{display: block;}
    .haeder-middle div { padding: 24px;}
    .haeder-middle{ margin-left: -20%;}
}
@media only screen and ( max-width:709px ){
    .haeder-middle{ display: flex; flex-direction: row-reverse; padding-left: 20px;}
    .haeder-middle-logo{ display:none; }
    #haeder-middle-right2{display: block;}
}
</style>