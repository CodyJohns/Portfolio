<template>
<div class="black">
    <div class="col-xs-12 h-60px white f-padding text-center">
        Copyright &copy; 2020-{{ getYear }} Cody Johns.
        &nbsp;&nbsp;&nbsp;<i class="fa fa-phone" aria-hidden="true"></i> (972) 201-7993
        &nbsp;&nbsp;&nbsp;<i class="fa fa-envelope" aria-hidden="true"></i> cjohns365@gmail.com
    </div>
</div>
</template>

<style>
.black {
    background: #12130F;
}

.h-60px {
    min-height: 60px;
}

.white {
    color: #f9f4f5;
}

.f-padding {
    padding: 20px 10px 40px 10px;
}
</style>

<script>
import moment from 'moment';

const Footer = {
    name: 'Footer',
    computed: {
        getYear() {
            return moment().format('Y');
        }
    }
}
export default Footer
</script>