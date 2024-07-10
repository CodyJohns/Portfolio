<template>
<div class="h-60px flagship-background p-o">
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
            <h4>AI playing Space Train</h4>
            <p>
                Skills used: Python, PyGame, NEAT-Python
            </p>
            <p>
                After seeing various programmers on YouTube using machine learning to train models to play games, I decided to try it myself. 
                I re-coded a game that I made in 2017, but never released officially, using Python's PyGame library.
            </p>
            <p>
                I wanted to use Neural Networks to play this game which has complex user input, I believed I could use a genetic machine 
                learning algorithm (<a target="_blank" href="https://en.wikipedia.org/wiki/Neuroevolution_of_augmenting_topologies">NEAT</a>) to do this.
            </p>
            <p>
                The trick to learning how to use NEAT, or any learning algorithm, is to identify the appropriate inputs. 
                These were the inputs I found most useful:
                <ul>
                    <li>Train position x</li>
                    <li>Train position y</li>
                    <li>True/False train shooting</li>
                    <li>Mouse position x</li>
                    <li>Mouse position y</li>
                    <li>The closest 3 enemy ships x and y coordinates, velocities, and relative distances to train</li>
                </ul>
            </p>
            <p>
                For a more thorough analysis, I suggest reading the README in the github repo.
            </p>
            <p>
                Source code: <a target="_blank" href="https://github.com/CodyJohns/NeatSpaceTrain">https://github.com/CodyJohns/NeatSpaceTrain</a>
            </p>
            <div>
                <iframe class="yt-video-m" src="https://www.youtube.com/embed/3rCui9JlyLA?si=x8CKqRUKneta5LzL" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
            </div>
        </div>
    </div>
</div>
</template>

<style>
.yt-video-m {
    width: 100%;
    aspect-ratio: 16/9;
}

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