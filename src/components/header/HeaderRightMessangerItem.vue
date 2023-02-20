<script>
    export default{
        data(){},
        props:['name','message']
    }

</script>

<template>
    <div class="box-messanger-amis">
        <div class="box-messanger-pas-amis-div1" style="position:relative;">
        <img src="../../assets/img/logo_fb.png" style="width:100;height:100%;border-radius:50%">
        <div style="width:15px;height:15px;border-radius:50%;background-color:#242526;;position:absolute;bottom:2px;right:0px">
            <div style="width:13px;height:13px;border-radius:50%;background-color:rgb(49 162 76);position:absolute;bottom:1px;right:1px"></div>
        </div>
        </div>
        <div class="box-messanger-pas-amis-div2">
            <span style="font-weight: 480;"> {{name}} </span><br>
            <small>  {{message}} </small> 
        </div>
    </div>
</template>

<style>

</style>