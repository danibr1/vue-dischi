<template>
    <div class="album text-center">
        <img class="img-fluid" :src="info.poster" :alt="info.title">
        
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