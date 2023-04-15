<template>
    <JumboComponent />
    <div class="content-bg">
        <div class="container py-4 px-0 ">
            <div class="d-flex flex-wrap justify-content-between gap-3 ms-4">
                <CardComponent :image="comic.thumb" :title="comic.series" v-for="(comic,index) in comicSeries" :key="index"/>
                
            </div>
        </div>
    </div>
    <div class="icon-box d-flex align-items-center">
        <div class="container py-2 px-0">
            <ul class="d-flex justify-content-around my-0 py-5">
                <li v-for="(link, index) in shopList" :key="index" class="d-flex align-items-center  ">
                    <div class="d-flex justify-content-center shopicon-box">
                        <img :src="link.icon" alt="">
                    </div>
                    <span class="text-uppercase text-white ms-3 ">{{ link.text }}</span>
                </li>
            </ul>
        </div>
    </div>
</template>

<script>
import CardComponent from './CardComponent.vue'
import JumboComponent from './JumboComponent.vue';
import { mainLinks } from '../data/data.js';
import { dcComics } from '../data/data.js';
export default {
    name: 'MainComponent',
    data() {
        return {
            comicSeries: [...dcComics],
            shopList: mainLinks,

        }
    },
    components: {
        JumboComponent,
        CardComponent

    }


}
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/variables' as *;

.content-bg {
    background-color: #1c1c1c;
}

.icon-box {
    background-color: $blue-bg;
    // height: 140px;

}

img {
    width: 100%;
    height: 100%;
    object-fit: contain;
}

span {
    font-size: .8rem;
    white-space: nowrap;
}


ul {
    list-style: none;
}


.shopicon-box{
    width: 50px;
    height: 50px;
}
</style>