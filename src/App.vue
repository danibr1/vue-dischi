<template>
    <div id="app">
        <Header />

        <AlbumsList />

    </div>
</template>

<script>
import Header from '@/components/Header';
import AlbumsList from '@/components/AlbumsList';

export default {
    name: 'App',
    components: {
        Header,
        AlbumsList,
    },
};
</script>

<style lang="scss">
    // BOOTSTRAP 
    @import '~bootstrap/scss/bootstrap';

    // FONT
    @import "~@fontsource/roboto/index.css"; // Weight 400.
    @import "~@fontsource/roboto/700.css"; // Weight 700.    

</style>
