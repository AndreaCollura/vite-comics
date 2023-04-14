<template>
    <div class="bg-white">
        <div class="container py-4 px-0">
            <div class="d-flex justify-content-between align-items-center m-0">
                <div class="logo">
                    <img src="/img/dc-logo.png" alt="">
                </div>
                <div>
                    <ul class="d-flex gap-4">
                        <li v-for="(link, index) in navList" :key="index" >
                            <a :href="link.url">{{ link.text }}</a>
                        </li>
                    </ul>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import { headerLinks } from '../data/data.js';
    export default {
        name: 'HeaderComponent',
        data(){
            return {
                navList: headerLinks

            }
        }

        
    }
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/variables' as *;

    li{
        list-style: none;
        a{
            text-decoration: none;
            color: black;
            text-transform: uppercase;
            font-size: .8rem;
            font-weight: bold;
            padding-bottom: 62px;

            &:hover {
                color: $blue-bg;
                border-bottom: 3px solid $blue-bg;
            }
        }
        
    }


    img {
        width: 80%;
    }
</style>