<template>
<div class="img_zoom">
    <div class="col-sm-12 position-relative bkg-white h-44">
        <button class="btn btn-close btn-light position-absolute" style="top:10px;right:20px;" @click="close"></button>
    </div>
    <div class="col-sm-12">
        <img :src="require(`@/assets/${imgObj.imgSrc}`)" class="img_info position-absolute" style="top: 50%;left: 50%;transform: translate(-50%, -50%);" />
    </div>
</div>
</template>

<style>
.img_zoom {
    width: 100vw;
    height: 100vh;
    position: fixed;
    top: 0px;
    left: 0px;
    background: rgba(0, 0, 0, 0.7);
}

.img_info {
    width: v-bind(imgObj.width);
    height: v-bind(imgObj.height)
}

.img_size {
    width: 100%;
}

.h-44 {
    height: 44px;
}

.bkg-white {
    background-color: #fafafa !important;
}
</style>

<script>
const ImageZoom = {
    name: 'ImageZoom',
    props: {
        imgObj: Object,
    },
    methods: {
        close() {
            this.$emit('close', false);
        }
    }
}
export default ImageZoom
</script>