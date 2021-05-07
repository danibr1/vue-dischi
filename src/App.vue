<template>
    <div id="app">
        <Header />

        <AlbumsList />

        <Album />

    </div>
</template>

<script>
import Header from '@/components/Header';
import AlbumsList from '@/components/AlbumsList';
import Album from '@/components/Album';




export default {
    name: 'App',
    components: {
        Header,
        AlbumsList,
        Album,

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
