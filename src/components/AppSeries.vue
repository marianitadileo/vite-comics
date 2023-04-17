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
        width: calc(100% / 6 - 20px);
        height: 100%;
        margin: 10px;
        padding: 10px;
        font-size: 1rem;
    }

    img {
       width: 100%;
       height: 200px; 
    }

    
</style>