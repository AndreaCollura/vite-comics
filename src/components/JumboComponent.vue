<template>
    <div class="jumbo-box">
        <div class="container h-100 label-fix py-4 px-0 ">
            <div class="current-label text-center text-white ">
                <h5 class="text-uppercase pt-2">current series</h5>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name:'JumboComponent',
        
    }
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/variables' as *;

    .jumbo-box{
        background-image: url(../assets/img/jumbotron.jpg);
        background-repeat: no-repeat;
        background-size: cover;
        height: 400px;
    }


    .laber-fix{
        position: absolute;
    }


    .current-label{
        width: 200px;
        height: 40px;
        background-color: $blue-bg ;
        text-align: center;
        position: relative;
        top: 355px;

    }

    h5{
        text-align: center;
    }

    

</style>