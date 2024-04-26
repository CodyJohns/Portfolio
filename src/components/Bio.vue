<template>
<div class="h-60-b plr bio-background" id="about">
    <div class="col-sm-6 offset-sm-3">
        <h2>{{ getGreetingByTimeOfDay }}!</h2>
        <p>
            I'm Cody Johns, Software Engineer with a BS in Computer Science from BYU.
        </p>
        <p>
            In my professional work, coursework, and personal projects I closely follow the principle of developing maintainable software. The software 
            that a company uses can make or break their business. That's why hiring the right software developers is a crucial task. A company needs reliable/trustworthy, knowledgeable, 
            and hardworking software developers. This is what I can offer and more.
        </p>
        <p>
            As a programmer who started in his high school days, I am passionate about what I do. I've programmed microcontrollers, Raspberry Pis, computer games, to websites and mobile smartphone apps.
        </p>
        <p>Here's some of the tools I've used:</p>
        <div class="row pb-4">
            <div class="col-sm-6 col-12">
                <ul>
                    <li>SpringBoot Web Framework</li>
                    <li>Express.JS</li>
                    <li>HTML & CSS</li>
                    <li>React.JS</li>
                    <li>React Native</li>
                    <li>Flutter</li>
                    <li>Vue.JS</li>
                    <li>Jenkins</li>
                    <li>Docker</li>
                    <li>C++</li>
                </ul>
            </div>
            <div class="col-sm-6 col-12">
                <ul>
                    <li>Python</li>
                    <li>Linux</li>
                    <li>AWS</li>
                    <li>Oracle Cloud</li>
                    <li>Drupal</li>
                    <li>PHP</li>
                    <li>Nginx</li>
                    <li>Apache</li>
                    <li>MySQL</li>
                    <li>PostgreSQL Vectors for LLMs</li>
                </ul>
            </div>
        </div>
        <p>Don't see what you need? I'm probably already learning it, or have plans to learn it in the future.</p>
        <p>So what are you waiting for? I'm one <a :href="'tel:' + getPhoneNumber.raw">phone call</a> from working on your project.</p>
    </div>
</div>
</template>

<style>
.plr {
    padding: 80px 40px 40px 40px;
}

.bio-background {
    background: url('@/assets/code-solid.webp');
    background-repeat: no-repeat;
    background-position: 110%;
    background-size: 60%;
}

a {
    text-decoration-style: dotted;
}

ul {
    margin-bottom: 0px;
}

@media only screen and (max-width: 500px) {
    .bio-background {
        background-size: 100%;
    }
}
</style>

<script>
import moment from "moment";

const Bio = {
    name: 'Bio',
    computed: {
        getGreetingByTimeOfDay() {
            let time = moment().hours();

            if(time >= 0 && time < 12)
                return "Good Morning";
            else if(time >= 12 && time < 17)
                return "Good Afternoon";
            else
                return "Good Evening";
        },
        getPhoneNumber() {
            return {
                raw: "9722017993",
                pretty: "(972) 201-7993"
            };
        }
    }
}
export default Bio
</script>