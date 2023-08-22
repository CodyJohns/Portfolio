<template>
<div class="flagship-background" id="projects">
    <div class="col-sm-10 offset-sm-1 h-60px p-o dflex">
        <div class="col-sm-6 offset-sm-1 p-i">
            <h4>EZ Budget</h4>
            <p>
                Skills used: React Native, Jenkins, Docker, SpringBoot Web, Oracle NoSQL Database
            </p>
            <p>
                <a href="https://ezbudget.app/" target="_blank">EZ Budget</a> is a smartphone app I launched in the summer of 2023.
            </p>
            <p>
                After being left unsatisfied by other budget planning and recording apps on the app store, I decided to code my own.
            </p>
            <p>
                Users can plan their budget by setting up calculated and variable expenses. 
            </p>
            <p>
                <strong>Calculated expenses</strong> can best be described as expenses that <strong>do not vary month to month</strong>. 
                Users can specify whether a calculated expense is an exact value or based off of a percentage of the gross or net income. 
            </p>
            <p>
                <strong>Variable expenses</strong> are the monthly expenses that <strong>can fluctuate from month to month</strong>, and as well as other unplanned expenses. 
            </p>
            <p>
                On a monthly basis, users will input their gross and net income and input what their preset calculated and variable expenses were. 
                Users can review what they spent the most on and what their average monthly income is.
            </p>
            <div class="row">
                <div class="col-12 col-sm-4">
                    <a href="https://play.google.com/store/apps/details?id=com.ezincometracker&pcampaignid=pcampaignidMKT-Other-global-all-co-prtnr-py-PartBadge-Mar2515-1" target="_blank"><img src="@/assets/google_play.png" class="google-play-btn" /></a>
                </div>
                <div class="col-12 col-sm-8">
                    <p class="ps-0 ps-sm-5 pt-4">Coming soon to iOS App Store</p>
                </div>
            </div>
        </div>
        <div class="col-sm-4 offset-sm-1 p-i">
            <div class="col-sm-12">
                <i>(Click to Zoom)</i>
            </div>
            <div class="col-sm-12">
                <img src="@/assets/ezbudget.png" class="img-l" @click="image_zoom('ezbudget.png')" />
            </div>
        </div>
    </div>
</div>
</template>

<style>
.flagship-background {
    background-color: #fafafa;
}
.img-l {
    height:600px;
}
.google-play-btn {
    width: 200px;
}
</style>

<script>
const Flagship = {
    name: 'Flagship',
    methods: {
        image_zoom(src) {
            this.$emit('image_zoom', {
                imgSrc: src,
                width: 'auto',
                height: '80vh'
            });
        }
    }
};

export default Flagship;
</script>