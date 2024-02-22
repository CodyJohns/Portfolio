<template>
<div class="gainsboro">
    <div class="h-60 code black-back d-flex align-items-center justify-content-start position-relative">
        <div class="col-sm-6 p-l text-start">
            <h4>Hello, I'm</h4>
            <h1>Cody Johns</h1>
            <h3>Software Engineer</h3>
            <br />
            <a href="https://drive.google.com/file/d/1UQxA8vjRKl7k1UnIcA37CRITqKoKL8YI/view?usp=sharing" target="_blank"><button class="btn btn-outline-light" style="margin-right:20px;">View Resume</button></a>
            <a href="#projects"><button class="btn btn-outline-light" style="margin-right:20px;">View Projects</button></a>
        </div>
        <div class="col-12 col-sm-12 text-center" style="position:absolute;bottom:30px;">
            <a class="null pe-3" href="#about">
                <i class="fa fa-arrow-down" aria-hidden="true"></i> 
                About Me
            </a>
            <a class="null ps-3 pe-3" href="https://github.com/CodyJohns" target="_blank">
                GitHub
                <i class="fa fa-github" aria-hidden="true"></i>
            </a>
            <a class="null ps-3" href="https://www.linkedin.com/in/cody-johns-61230ab2/" target="_blank">
                LinkedIn
                <i class="fa fa-linkedin" aria-hidden="true"></i>
            </a>
        </div>
    </div>
</div>
</template>

<style>
.black-back {
    background: linear-gradient(135deg, #1a759f 20%, #34a0a4 70%, #52b69a 70%);
    color: #F9F4F5;
}

.code {
    border-bottom-left-radius: 10px;
    border-bottom-right-radius: 10px;
}

.p-l {
    padding-left: 18%;
}

.h-60 {
    min-height: 600px;
    height: 80vh;
}

.null {
    text-decoration: unset;
    color: #f9f4f5;
}

.null:hover {
    color: #CCC;
}

h1 {
    font-size: 72px;
}

h3 {
    font-size: 32px;
}

@media only screen and (max-width: 540px) {
    .p-l {
        padding-left: 10%;
    }
}

@media only screen and (min-width:541px) and (max-width: 1400px) {
    .p-l {
        padding-left:12%;
    }
}
</style>

<script>
const Landing = {
    name: 'Landing',
}
export default Landing
</script>