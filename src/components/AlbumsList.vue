<template>
    <section class="album-list">

    </section>
</template>

<script>
import axios from 'axios';
// import axios from 'axios';
// import Single Album component - import Loader from '@/components/Album';
// import loader - import Loader from '@/components/Loader';


export default {
    name: 'AlbumsList',
    component: {
        // Single Album 
        // Loader
    },
    data () {
        return {
            apiUrl: 'https://flynn.boolean.careers/exercises/api/array/music',
            albumList: [],
            loading: true,
        };
    },
    created () {
        this.getAlbums();
    },
    methods: {
        getAlbums() {
            /**
             * API Call
             */
            axios
            .get(this.apiUrl)
            .then((res) => {
                console.log(res.data);
                this.albumList = res.data;
                this.loading = false;
            })
            .catch((err) => {
                console.log('Error', err);
            });
        },
    },
}
</script>


<style lang="scss">
    @import '../styles/vars';
    @import '../styles/general';

</style>