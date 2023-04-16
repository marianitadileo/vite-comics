<script>
export default {
    name: "AppSeries",
    props: {
        thumb: String, 
        serie: String
    }
}
</script>

<template>
    <div class="card">
        <img :src="thumb">
        <h3>{{ serie }}</h3>
    </div>
</template>

<style scoped lang="scss">
    .card {
        width: calc(100% / 6 - 10px);
        margin: 5px;
        padding: 10px;
    }

    img {
       width: 100%;
       
    }

    
</style>