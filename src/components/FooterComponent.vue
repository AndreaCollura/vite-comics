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
            <div class="w-50 logo-box">
                <img class="foot-logo" src="../assets/img/dc-logo-bg.png" alt="">
            </div>
        </div>
    </div>
    <div class="footerBot d-flex align-items-center  ">
        <div class="container py-3 px-0 ">
            <div class="d-flex justify-content-between align-items-center m-0">
                <div>
                    <button class="">sign-up now!</button>
                </div>
                <div>
                    <ul class="d-flex align-items-center mb-0">
                        <li class="me-3 text-uppercase">follow us</li>
                        <div>
                            <a v-for="(icon,index) in socialList" :key="icon" class="me-2" href="">
                                <img :src="icon.text" alt="">
                            </a>
                        </div>
                    </ul>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import {footerLinks} from '../data/data.js';
import {socialLinks} from '../data/data.js';

    export default {
        name: 'FooterComponent',
        data(){
            return {
                footerList: footerLinks,
                socialList: socialLinks,
                
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
        color: $blue-bg;
        a{
            text-decoration: none;
            color: rgba(255, 255, 255, 0.519);
            font-size: .7rem;
            
            
        }
        
    }

    .linksBox {
        width: 400px;
        height: 300px;
    }


    .logo-box{
        height: 400px;
        position: relative;
        overflow: hidden;
    }

    .foot-logo{
        position: absolute;
        top:-90px;
    }

    button{
        width: 140px;
        height: 40px;
        border: 2px solid $blue-bg;
        margin-left: 10px;
        background-color: transparent;
        color: white;
        text-transform: uppercase;
    }
    

</style>