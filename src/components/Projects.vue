<template>
<div class="h-60px gainsboro p-o">
    <div class="col-sm-9 dflex" style="margin:0 auto;">
        <div class="col-sm-5 p-i">
            <h4>Speaker Approval System</h4>
            <p>
                Skills used: PHP, MySQL, Javascript, Drupal Webforms, Drupal Views
            </p>
            <p>
                I refactored the code of a Drupal module for the BYU McKay School of Education and added features. 
                The module allows for the school faculty to submit a Speaker Request. 
            </p>
            <p>
                The request is sent via email to the designated approvers who review the information which the module displays. 
                The module displays webpages which contain request information and graphics that are updated to display the current status 
                of the request.
            </p>
            <p>
                The requestor and approvers can access a main page where they can all see their respective requests made/awaiting for them.
            </p>
            <i>(Click to Zoom)</i>
            <img src="@/assets/speaker_approval.png" style="width:100%;" @click="image_zoom('speaker_approval.png')" />
        </div>
        <div class="col-sm-5 offset-sm-2 p-i p-t">
            <h4>Scholarship Auto Awarding System</h4>
            <p>
                Skills used: PHP, Vue.Js, MySQL, Drupal Webforms
            </p>
            <p>
                The BYU McKay School of Education previously awarded scholarships manually- a process which would take many weeks to complete. 
                I worked on a team to help create a Drupal Module using Drupal's back-end PHP REST-API with the front-end using Vue.Js for the interactive UI. 
            </p>
            <p>
                The project had a lot of complex logic. There are many ways to award scholarships to applicants, and we had to make different ways of sorting the applicants and the scholarships.
                The awarding algorithm can award by most qualified in a career program and evenly among each program.
            </p>
            <p>    
                The scholarship committee members can use the system to generate 
                multiple award outcomes and can choose between the best results.
            </p>
            <i>(Click to Zoom)</i>
            <img src="@/assets/auto_award.png" style="width:100%;" @click="image_zoom('auto_award.png')" />
        </div>
    </div>
</div>
</template>

<style>
.star-command {
    background: #2380BE;
}

img {
    border-radius: 4px;
    cursor: pointer;
}

i {
    margin-top: 20px;
    font-size: 10px;
}

@media only screen and (max-width: 500px) {
    .p-t {
        padding-top: 40px !important;
    }
}
</style>

<script>
const Projects = {
    name: 'Projects',
    methods: {
        image_zoom(src) {
            this.$emit('image_zoom', {
                imgSrc: src,
                width: '80%',
                height: 'auto'
            });
        }
    }
}
export default Projects
</script>