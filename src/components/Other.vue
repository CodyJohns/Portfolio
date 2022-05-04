<template>
<div class="col-sm-10 offset-sm-1 h-60px other-background p-o dflex">
    <div class="col-sm-6 offset-sm-1 p-i">
        <h4>The Champs Gaming Events</h4>
        <p>
            Skills used: Nginx, Node.Js, Express.Js, Axios, Bcrypt.Js, Python, MySQL.
        </p>
        <p>
            <a href="https://thechamps.co/" target="_blank">The Champs</a> is a website where gamers from any platform can create, join, and play in tournaments/matches with others. 
        </p>
        <p>
            I helped create webpages that use axios to access the back end Node.js server, wrote Javascript Timers, used Javascript Libraries such as Bcrypt.js for password hashing, Moment.js to handle timezones, and used the Paypal REST-API to process payments. 
            All information was kept in a MySQL database which I helped manage and setup. Python scripts were used to run database operations such as payment logs, which are setup to be downloaded and uploaded to paypal, and delete old uploaded user pictures for tournament/match evidence. 
            The Python scripts were run using linux cron jobs.
        </p>
    </div>
    <div class="col-sm-4 offset-sm-1 p-i">
        <div class="col-sm-12">
            <i>(Click to Zoom)</i>
        </div>
        <div class="col-sm-12">
            <img src="@/assets/champs.png" class="img-m" @click="image_zoom('champs.png')" />
        </div>
    </div>
</div>
</template>

<style>
.p-o {
    padding: 80px 0px 80px 0px;
}

.img-m {
    height:400px;
}

.dflex {
    display:flex;
    justify-content:center;
}

.other-background {
    background: url('@/assets/code-branch-solid.webp');
    background-repeat: no-repeat;
    background-position: 20%;
    background-size: 50%;
}

@media only screen and (max-width: 500px) {
    .other-background {
        background-size: 90%;
    }
    .dflex {
        display:block;
    }
    .p-i {
        padding:0px 40px 0px 40px;
    }
    .img-m {
        height:unset;
        width:100%;
        padding-top:40px;
        padding-bottom:40px;
    }
} 
</style>

<script>
const Other = {
    name: 'Other',
    methods: {
        image_zoom(src) {
            this.$emit('image_zoom', {
                imgSrc: src,
                width: 'auto',
                height: '80vh'
            });
        }
    }
}
export default Other
</script>