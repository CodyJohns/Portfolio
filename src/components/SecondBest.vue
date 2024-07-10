<template>
<div class="gainsboro">
    <div class="col-sm-10 offset-sm-1 h-60px p-o dflex">
        <div class="col-sm-4 offset-sm-1 p-i">
            <div class="position-relative" v-bind:class="{ 'cheight-hidden' : !showing }">
                <h4>Scholarship Auto Awarding System</h4>
                <p>
                    Skills used: PHP, Vue.Js, MySQL, Drupal Webforms
                </p>
                <p>
                    The BYU McKay School of Education previously awarded scholarships manually&mdash; a process which would take many full days to complete. 
                    I collaborated with a team of developers to help create a Drupal Module using Drupal's back-end PHP REST-API with the front-end using Vue.Js for an interactive UI with many configurable options. 
                </p>
                <p>
                    The system had various complex requirements. It had to be efficient, quick, and most importantly accurate. 
                    We made sure to test that awards would only be made if they had to. The awarding code was analyzed and improved to remove any slow code and unnecessary for-loops. 
                    One of the challenges we ran into was that the scholarships with stricter requirements and criteria weren't being completely dispensed to the candidates they 
                    correspond to most.
                </p>
                <p>
                    A graph-based awarding algorithm was devised to handle this. The algorithm would connect each scholarship to candidates that would qualify for it. 
                    Depending on the number of edges (connections) between the scholarship and applicants, the algorithm would then find the scholarships with fewer applicants and award to those immediately. 
                    This resulted in all the funds being awarded with very little manual awarding.
                </p>
                <p>
                    After awarding on the graph-based approach, the system would continue awarding by an "evenly" strategy where a scholarship is selected and a single most qualified applicant is chosen. 
                    This repeats until all remaining scholarships are completely diminished or have no more applicants.
                </p>
                <div v-if="!showing" class="col-12 position-absolute text-center collapseable-btn" style="height: 24px;bottom: -2px;"></div>
            </div>
            <div class="col-12 text-center c-link">
                <div class="pt-2">
                    <a role="button" v-if="!showing" @click="showing = true">Show More</a>
                    <a role="button" v-else @click="showing = false">Show Less</a>
                </div>
            </div>
        </div>
        <div class="col-sm-6 offset-sm-1 p-i">
            <div class="col-sm-12">
                <i>(Click to Zoom)</i>
            </div>
            <div class="col-sm-12">
                <img src="@/assets/auto_award.png" class="img-s" @click="image_zoom('auto_award.png')" />
            </div>
        </div>
    </div>
</div>
</template>

<style>
.cheight-hidden {
    height: 400px;
    overflow: hidden;
}

.collapseable-btn {
    background: linear-gradient(0deg, #f5f5f5ff, #f5f5f500);
}

.c-link a {
    text-decoration: dotted !important;
    text-decoration-style: dotted !important;
    color: rgba(var(--bs-link-color-rgb), var(--bs-link-opacity, 1)) !important;
}
</style>

<script>
const SecondBest = {
    name: 'SecondBest',
    data: () => {
        return {
            showing: false
        }
    },
    methods: {
        image_zoom(src) {
            this.$emit('image_zoom', {
                imgSrc: src,
                width: '80%',
                height: 'auto'
            });
        }
    }
};
export default SecondBest;
</script>