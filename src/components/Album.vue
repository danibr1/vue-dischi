<template>
    <div class="album text-center">
        
        <div class="poster">
            <img class="img-fluid" :src="info.poster" :alt="info.title">
        </div>
        
        <div class="details">
            <h3 class="fw-bold">{{ info.title }}</h3>
            <div>{{ info.author }}</div>
            <div>{{ info.year }}</div>
            <div>{{ info.genre }}</div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Album',
    props: ["info"],
};
</script>

<style scoped lang="scss">
    
</style>