<template>
<div class="col-xs-12 h-60p gainsboro responsive-font borders" style="color:#afb1b4;display:flex;align-items:center;justify-content:center;">
    <span>VUE.JS</span>
    <span>NODE.JS</span>
    <span>MySQL</span>
    <span>PHP</span>
    <span>DRUPAL</span> 
    <span>REST-APIs</span>
    <span>PYTHON</span>
    <span>C++</span>
</div>
</template>

<style>
.gainsboro {
    background: #DDDFE4;
}

.borders {
    border-bottom-left-radius: 10px;
    border-bottom-right-radius: 10px;
}

.h-60p {
    height: 60px;
}

.responsive-font {
    font-size: 100%;
}

span {
    font-weight: bold;
    padding:0px 1% 0px 1%;
}

span:hover {
    color: #CCC;
}

@media only screen and (max-width: 540px) {
    .responsive-font {
        font-size: 70%;
    }
}
</style>

<script>
const Technologies = {
    name: 'Technologies',
}
export default Technologies
</script>