<template>
    <div class="col-12">
        <div class="card">
            <div class="card-body">
                <div class="card-image">
                    <img :src="" alt="">
                </div>
                <div class="card-title">
                    {{ title }}
                </div>
            </div>
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

</style>