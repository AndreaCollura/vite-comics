<template>
    <div class="footerTop">
        <div class="container d-flex px-0 ">
            <div class="py-3 w-50 mx-0">
                <div class="d-flex flex-column flex-wrap linksBox">
                    <ul class="px-0" v-for="(list, index) in footerList" :key="index">
                        <li class="text-white text-uppercase">{{ list.title }}</li>
                        <li v-for="(item, i) in list.links" :key="i">
                            <a :href="item.url">{{ item.text }}</a>
                        </li>
                    </ul>
                </div>
            </div>
            <div class="w-50  debug">
                <img src="" alt="">
            </div>
        </div>
    </div>
    <div class="footerBot d-flex align-items-center debug ">
        <div class="container py-3 px-0 debug">
            <div class="d-flex justify-content-between align-items-center m-0">
                <div>
                    <button class="btn btn-primary"></button>
                </div>
                <div>
                    <ul>
                        <li></li>
                    </ul>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import {footerLinks} from '../data/data.js';
    export default {
        name: 'FooterComponent',
        data(){
            return {
                footerList: footerLinks
            }
        }
        
    }
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/variables' as *;
    .footerTop {
        background-image: url(../assets/img/footer-bg.jpg);
        background-repeat: no-repeat;
        background-size: cover;
        
        
        
        
        
    }

    .footerBot{
        background-color: $grey-bg;
        height: 120px;
        
    }

    li{
        list-style: none;
        a{
            text-decoration: none;
            color: rgba(255, 255, 255, 0.519);
            font-size: .7rem;
            
            
        }
        
    }

    .linksBox{
        width: 400px;
        height: 300px;
    }
    

</style>