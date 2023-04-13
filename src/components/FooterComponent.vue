<template>
    <div class="footerTop-bg debug">
        <div class="container d-flex py-4 px-0 debug">
            <div class="d-flex justify-content-start debug m-0">
                <div>
                    <ul>
                        <li></li>
                    </ul>
                </div>
            </div>
            <div class=" debug">
                <img src="" alt="">
                
            </div>
        </div>
    </div>
    <div class="footerBot-bg debug ">
        <div class="container py-3 px-0 debug">
            <div class="d-flex justify-content-between align-items-center m-0">
                <div>
                    <button></button>
                </div>
                <div>
                    <ul >
                        <li></li>
                    </ul>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        
    }
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/variables' as *;
    .footerTop-bg {
        background-image: url(../assets/img/footer-bg.jpg);
        background-repeat: no-repeat;
        background-size: cover;
    }

    .footerBot-bg{
        background-color: $grey-bg;
    }

    img{
        
    }

</style>