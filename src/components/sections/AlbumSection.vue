<template>
    <section>
        <div class="container">
            <div class="albums">
                <AlbumCard class="albums__list" v-for="(album, index) in FilteredGenreAlbum" :key="index" :album="album"/>
            </div>
        </div>
    </section>
</template>

<script>
    import axios from 'axios';
    import AlbumCard from '../commons/AlbumCard';
    import select from "../../shared/select";

    export default {
        name: 'AlbumSection',
        components: {
            AlbumCard,
        },
        data() {
            return {
                albums: [],
                select
            };
        },
        created() {
            axios.get('https://flynn.boolean.careers/exercises/api/array/music')
            .then((response) => {
                this.albums = response.data.response;
            })
        },
        computed: {
            FilteredGenreAlbum() {
                if (this.select.text === '') {
                    return this.albums.filter(album => album.genre.toLowerCase() === this.select.selected || this.select.selected === "all"); 
                }
                return this.albums.filter(album => album.author.toLowerCase().includes(this.select.text.toLowerCase()));
            },
        }
    }
</script>

<style lang="scss" scoped>
    .albums {
        display: flex;
        flex-wrap: wrap;
        padding: 0 1.875rem;

        &__list {
            width: calc(100% / 5 - 1.875rem);
            margin: .9375rem;

            @media screen and (max-width: 75rem) {
                & {
                    width: calc(100% / 5 - 1.875rem);
                }
            }

            @media screen and (max-width: 62rem) {
                & {
                    width: calc(100% / 4 - 1.875rem);
                }
            }

            @media screen and (max-width: 48rem) {
                & {
                    width: calc(100% / 3 - 1.875rem);
                }
            }

            @media screen and (max-width: 36rem) {
                & {
                    width: calc(100% / 2 - 1.875rem);
                }
            }

            @media screen and (max-width: 25rem) {
                & {
                    width: calc(100% - 1.875rem);
                }
            }
        }
    }
</style>