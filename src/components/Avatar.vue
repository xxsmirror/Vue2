<template>
  <img
    class="img-avatar"
    :src="url" :style="{
    weight:weight+'px',
    height:height+'px'
  }">
</template>

<script>
export default {
    props:{
        url:{
            type:String,
            require:true
        },
        height:{
            type:Number,
            default:150
        },
        weight:{
            type:Number
        },
    }
}
</script>

<style scpoed>
    .img-avatar{
        border-radius: 50%;
        object-fit: cover;
        display: block;
    }
</style>