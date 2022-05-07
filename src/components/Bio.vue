<template>
<div class="h-60-b plr bio-background" id="about">
    <div class="col-sm-6 offset-sm-3">
        <h2>Hello!</h2>
        <p>
            I'm a BYU student majoring in Computer Science. 
            I have been coding since I was in High School and I currently work for the McKay School of Education as
            a Full Stack Web Developer.
        </p>
        <div class="col-sm-6 offset-sm-3">
            <p>
                I have skills/experiences with:
                <ul>
                    <li>HTML 5 + CSS</li>
                    <li>Node.Js</li>
                    <li>Vue.Js</li>
                    <li>Git</li>
                    <li>PHP</li>
                    <li>Drupal</li>
                    <li>MySQL</li>
                    <li>Python</li>
                    <li>C++</li>
                    <li>Java</li>
                    <li>Debian-Based Linux Systems</li>
                </ul>
            </p>
        </div>
        <p>
        Learning new technologies is a skill that every Developer must have. I work hard and put 100% effort in meeting the goals and deadlines.
        </p>
    </div>
</div>
</template>

<style>
.plr {
    padding: 80px 40px 40px 40px;
}

.h-60-b {
    max-height: 1000px;
}

.bio-background {
    background: url('@/assets/code-solid.webp');
    background-repeat: no-repeat;
    background-position: 110%;
    background-size: 60%;
}

@media only screen and (max-width: 500px) {
    .bio-background {
        background-size: 100%;
    }
}    
</style>

<script>
const Bio = {
    name: 'Bio',
}
export default Bio
</script>