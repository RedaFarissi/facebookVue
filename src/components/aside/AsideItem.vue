<script>
    export default{
        data(){

        },
        props:['icon','name']
    }
</script>

<template>
    <a class="content-aside">
        <div class="content-aside-style" style="margin:7px">
            <div class="material-icons icons-tags">{{ icon }}</div>
        </div>
        <div id="user_name m-3" style="font-weight:520;"> {{ name }} </div>
    </a>
</template>

<style></style>