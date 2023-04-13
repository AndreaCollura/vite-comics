<template>
    <div class="content-bg">
        <div class="container py-4 px-0 ">
            <div class="d-flex justify-content-start m-0">
                <div>
                    <h2 class="py-3 text-white"><i class="fa-solid fa-arrow-right "></i>Content goes here<i class="fa-solid fa-arrow-left"></i></h2>
                </div>
            </div>
        </div>
    </div>
    <div class="debug iconBox d-flex align-items-center">
        <div class="container py-5 px-0 debug">
            <div>
                <div>
                    <!-- fare un v-for -->
                    <ul class="d-flex justify-content-around">
                        <li v-for="(link, index) in shopList" :key="index"   class="d-flex align-items-center">
                            <img :src="'../assets/img/buy'+ link.icon" alt="">
                            <span class="text-uppercase text-white ms-2 ">{{link.text}}</span>
                        </li>
                    </ul>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import { mainLinks } from '../data/data.js';
    export default {
        name: 'MainComponent',
        data(){
            return {
                shopList: mainLinks,
            }
        }

        
    }
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/variables' as *;
    .content-bg{
        background-color: #1c1c1c;
    }

    .iconBox{
        background-color: $blue-bg;
        height: 140px;

    }

    img{
        width: 20%;
    }

    span{
        font-size: .8rem;
        white-space: nowrap;
    }
</style>