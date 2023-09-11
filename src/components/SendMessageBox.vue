<script>
    export default{
        data(){
            return{ }
        }, 
        props:['send_message_box','clearMessageBox'],
        computed: {
          items_loop_number() {
            return Array.from({ length: this.send_message_box }, (_, index) => index);
          },
        },
    }
</script> 

<template>
<footer v-if="send_message_box > 0">    
    <div v-for="(item, index) in items_loop_number" :key="index">
        <div class="sending">
        <div class="sending-header">
            <div class="sending-header-part1">
                <div>
                    <div class="material-icons" style="font-size: 34px;"> account_circle </div>
                    <div class="en-lign" style="position:absolute;top:24px;left:29px;width:13px;height:13px;">
                        <div style="width:10px;height:10px;"></div>
                    </div>
                </div>
                <div style="margin-left:6px">
                    <div style="font-size:80%; font-weight:540;"> User Name </div>
                    <div style="font-size:60%;"> en ligne </div>
                </div>
            </div>
            <div class="sending-header-part2">
                <div class="styl_icons">
                    <div class="material-icons" style="font-size: 99%;"> call </div>
                </div>
                <div class="styl_icons">
                    <div class="material-icons" style="font-size: 99%;"> videocam </div>
                </div>
                <div class="styl_icons">
                    <div class="material-icons" style="font-size: 99%;"> remove  </div>
                </div>
                <div class="styl_icons" @click="clearMessageBox">
                    <div class="material-icons" style="font-size: 99%;"> clear </div>
                </div>
            </div>    
        </div>
        <div class="HR"></div>
        <div class="sending-profile-content">
            <img src="../assets/img/logo_fb.png"/>
            <div class="en-lign">
                <div>  </div>
            </div>
        </div>
        <div style="text-align:center;margin-top:106px;">
            <div style="font-weight:500;color:rgba(255 255 255/90%);">User Name</div>
            <div style="color:rgba(255 255 255/65%)"><small><small>Vous êtes amis sur Facebook<br>Habite à Sidi Sliman, Kenitra, Morocco<br>Sidi Slimane (Maroc)</small></small></div>
        </div>
        <div class="messaGe-send">
            <div class="material-icons" onclick=""> add_circle_outline </div>
            <div class="material-icons" onclick=""> collections </div>
            <div class="material-icons" onclick=""> sentiment_satisfied </div>
            <div class="material-icons" onclick=""> gif_box </div>
            <textarea placeholder="Aa" id="text-area-message"></textarea>
            <div class="material-icons"  onclick=""> thumb_up </div>
        </div>
    </div>
    </div>    
    
</footer>
</template>

<style>
footer{ display:flex;flex-direction: row-reverse;float:right;
    width:max-content;height:443px;position:fixed;bottom:0px;right:80px;}
.sending{ width:8.7cm;height:100%;background-color:rgb(36 37 38);border-radius:7px  7px 0px 0px;margin-left:9px;box-shadow:-1px -1px 20px rgba(0 0 0/50%); position: relative;}
.sending-header{display:flex;justify-content:space-between;padding:6px 0px;background-color:rgb(36 37 38);
    color:rgba(255 255 255/75%);border-radius:7px  7px 0px 0px;}
.sending-header-part1{display:flex;align-items:center;margin-left:7px;padding-right:2px;min-width:46%;border-radius:6px; }
.sending-header-part1:hover{  background-color: rgba(255 255 255/9%);  }
.sending-header-part2{  display:flex; margin-right: 10px; padding-top:4px; }
.styl_icons{width:26px;height:26px;border-radius: 50%;color:rgba(255 255 255/40%);
    display:flex;align-items:center;justify-content:center;}
.styl_icons:hover{background-color:rgba(255 255 255/9%); cursor:pointer;}
.sending-profile-content{width:60px;height:60px;border-radius:50%;position:absolute;margin-left:calc(50% - 32px);margin-top:45px;}
.sending-profile-content img{width:100%;height:100%;border-radius:50%;}
.en-lign{width: 16px;height: 16px;background-color:rgb(36 37 38);border-radius:50%; position:absolute;right:0px;bottom:3px;}
.en-lign div{width: 13px;height: 13px; background-color:rgb(49 162 76);border-radius:50%;margin: 1.5px;}
.HR{ height:0.4px; background-color:rgba(255 255 255/20%); box-shadow:0.5px 0.5px 2px rgba(0 0 0/80%); }
.messaGe-send{color:rgba(255 255 255/55%);width:calc(100% - 9px);height:40px;position:absolute;bottom:9px;
    display:flex;align-items:center;justify-content:space-between;padding:0px 8.5px; }
.messaGe-send textarea{height:80%;border-radius:20px;resize:none;outline:none;padding:2px 7px;height: 34px;
    width:150px;margin:0px 4px;background-color:rgb(58 59 60);border:none;color:rgba(255 255 255/75%)}
.messaGe-send div{ cursor: pointer;}
</style>