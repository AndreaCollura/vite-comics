<template>
    <div class="comic-box d-flex flex-column ms-2 mt-2">
        <div class="comic">
            <img :src="image">
        </div>
        <div class="mt-3" >
            <span class="text-white text-uppercase small">{{title}}</span>
        </div>
    </div>
    
</template>

<script>
export default {
    name: 'CardComponent',
    props: ['image', 'title']

}
</script>

<style lang="scss" scoped>
    .comic-box{
        width: 180px;
    }
    

    .comic{
        width: 180px;
        height: 170px;
        overflow-y: hidden;

    }
    img{
        width: 100%;
        
    }
    span{
        font-size: .7rem;
    }
    
    
</style>