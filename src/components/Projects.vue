<template>
<div class="h-60px gainsboro p-o">
    <div class="col-sm-9 dflex" style="margin:0 auto;">
        <div class="col-sm-5 p-i">
            <h4>Regex Generation using ChatGPT</h4>
            <p>
                Skills used: ReactJS, OpenAI API, OCI Functions using Fn Project, Java
            </p>
            <p>
                <a href="https://regex-gen.cdjmdev.com/" target="_blank">Regex-GPT</a>: I coded a quick web app that allows a user to input a prompt for regular expression generation.
                The app allows the user to add test cases to check the regex against custom test cases.
                It also maintains a history of returned regular expressions in case the user wants to
                load a previous expression.
            </p>
            <p>
                The front-end was made using ReactJS. The backend uses an Oracle Cloud Serverless function to call the OpenAI API and serve the
                response to the user.
            </p>
            <p>
                The repositories for the code can be found on GitHub:
                <ul>
                    <li>Front-end: <a href="https://github.com/CodyJohns/Regex-GPT-App" target="_blank">https://github.com/CodyJohns/Regex-GPT-App</a></li>
                    <li>Back-end: <a href="https://github.com/CodyJohns/Regex-GPT-Query-Controller" target="_blank">https://github.com/CodyJohns/Regex-GPT-Query-Controller</a></li>
                </ul>
            </p>
            <i>(Click to Zoom)</i>
            <img src="@/assets/regex-gpt.png" style="width:100%;" @click="image_zoom('regex-gpt.png')" />
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