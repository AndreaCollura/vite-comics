<template>
    <div class="debug content-bg">
        <div class="container py-4 px-0 debug">
            <div class="d-flex justify-content-start m-0">
                <div>
                    <h2 class="py-3 text-white"><i class="fa-solid fa-arrow-right "></i>Content goes here<i class="fa-solid fa-arrow-left"></i></h2>
                </div>
            </div>
        </div>
    </div>
    <div class="debug iconBox-bg">
        <div class="container py-4 px-0 debug">
            <div class="d-flex justify-content-start m-0">
                <div>
                    <!-- fare un v-for -->
                    <ul >
                        <li class="d-flex align-items-center">
                            <img src="../assets/img/buy-comics-digital-comics.png" alt="">
                            <span class="text-uppercase text-white ms-2 fw-semibold">digital comics</span>
                        </li>
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
    .content-bg{
        background-color: #1c1c1c;
    }

    .iconBox-bg{
        background-color: $blue-bg;

    }

    img{
        width: 20%;
    }

</style>