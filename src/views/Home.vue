<template>
    <div class="fullvh">
        <div class="grid">
            <div class="left">
                <p class="heading text-center text-white" style="width:50%;">I Build
                    website and apps</p>
                <p class="text-red">Abhishek Bhardwaj |
                    Web Designer and Developer</p>
                <div class="flex-row">
                   <router-link to="/contact" class="button red">Contact </router-link>
         
                    <a class="button-2">Resume</a>
                </div>
            </div>
            <div class="right">
                <img src="https://graph.facebook.com/100005873828354/picture?width=400&height=400" alt="">
            </div>
        </div>
    </div>

</template>
<script>
    export default {
        data() {
            return {

            }
        }
    }
</script>
<style lang="scss" scoped>
    .grid {
        display: grid;
        grid-template-columns: 1fr 1fr;
        grid-template-rows: 1fr;
        grid-template-areas: "left right";
        height: 100%;
    }

    .left {
        grid-area: left;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;

    }

    .right {
        grid-area: right;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        img{
            mix-blend-mode: normal;
            backdrop-filter: blur(1px);
            border-radius: 50%;
            //opacity: 50%;
            filter: brightness(.8) blur(0px);
transform: matrix(-1, 0, 0, 1, 0, 0);
        }
    }


@media screen and (max-width: 700px) {
    .text-red{
        margin: 20px;
    }
    .grid{
        display: flex;
        flex-direction: column-reverse;
        justify-content: center;
        align-items: center;
        
    }
    .right{
        display: none;
    }
    .heading{
        font-size:4rem;
    }
}
</style>