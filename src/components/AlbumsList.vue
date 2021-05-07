<template>
    <section class="album-list">
        <div v-if ="!loading" class="row">
            <!-- ALBUMS -->
            <Album
                class="col-12"
                v-for="(album, index) in albumList"
                :key="index"
                :info='album'
            />
        </div>
        <div v-else>Loading...</div>

    </section>
</template>

<script>
import axios from 'axios';
import Album from '@/components/Album';


export default {
    name: 'AlbumsList',
    components: {
        Album,
    },
    data() {
        return {
            apiUrl: 'https://flynn.boolean.careers/exercises/api/array/music',
            albumList: [],
            loading: true,
        };
    },
    created() {
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
                    console.log(res.data.response);
                    this.albumList = res.data.response;
                    this.loading = false;
                })
                .catch((err) => {
                    console.log('Error', err);
                });
        },
    },
};
</script>

<style lang="scss">
@import '../styles/vars';
@import '../styles/general';

.album-list {
    background: $bg-color;
    color: $second-text-color;
    padding: 120px 75px 30px;
}
</style>
