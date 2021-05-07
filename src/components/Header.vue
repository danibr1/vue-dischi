<template>
    <header class="header d-flex align-items-center">
        <a :href="logo.url">
            <img class="img-fluid" :src="logo.image" :alt="logo.text" />
        </a>
    </header>
</template>

<script>
export default {
    name: 'Header',
    data() {
        return {
            logo: {
                image: require('@/assets/img/logo.png'),
                url: '/',
                text: 'Spotify',
            },
        };
    },
};
</script>

<style scoped lang="scss">
@import '../styles/vars';
@import '../styles/general';

.header {
    background: $second-bg-color;
}

img {
    height: 45px;
    margin: 10px;
}
</style>
