<template>
<div class="col-sm-10 offset-sm-1 h-60px other-background p-o dflex">
    <div class="col-sm-6 offset-sm-1 p-i">
        <h4>Itigaria</h4>
        <p>
            Skills used: C++, SDL2 open source computer graphics library.
        </p>
        <p>
            <a href="https://cjx.itch.io/itigaria" target="_blank">Itigaria</a> is an Arkanoid clone I made in the summer of 2020.
        </p>
        <p>
            I programmed a clone of the old arcade game, Arkanoid. There are no sprites (except the font letters) because I wanted to keep the game simple and focus on programming the physics of the ball and blocks.
        </p>
        <p>
            Along with the game is included a level editing executable as well, although it is extremely primitive.
        </p>
        <p>
            This clone does vary from the original game by using 10 different types of blocks. The orange blocks do not break, while the gray blocks take two hits to break. 
            The rainbow blocks when hit release a powerup which will give one of the following abilities when caught by the paddle:
            <ul>
                <li>A larger paddle</li>
                <li>A faster moving paddle</li>
                <li>3 ball spawn</li>
            </ul>
        </p>
        <p>
            The pink blocks blink on and off allowing the ball to collide with it when on and allowing it to pass through when off.
            All other blocks only give different amounts of points depending on the color.
        </p>
    </div>
    <div class="col-sm-4 offset-sm-1 p-i">
        <div class="col-sm-12">
            <i>(Click to Zoom)</i>
        </div>
        <div class="col-sm-12">
            <img src="@/assets/itigaria.png" class="img-m" @click="image_zoom('itigaria.png')" />
        </div>
    </div>
</div>
</template>

<style>
.p-o {
    padding: 80px 0px 80px 0px;
}

.img-m {
    height: 400px;
}

.img-s {
    height:360px;
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
    .img-s {
        height:unset;
        width:100%;
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