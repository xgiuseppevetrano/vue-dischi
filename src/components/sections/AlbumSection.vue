<template>
    <section>
        <div class="container">
            <div class="albums">
                <AlbumCard class="albums__list" v-for="(album, index) in albums" :key="index" :album="album"/>
            </div>
        </div>
    </section>
</template>

<script>
    import axios from 'axios';
    import AlbumCard from '../commons/AlbumCard';

    export default {
        name: 'AlbumSection',
        components: {
            AlbumCard,
        },
        data() {
            return {
                albums: [],
            };
        },
        created() {
            axios.get('https://flynn.boolean.careers/exercises/api/array/music')
            .then((response) => {
                this.albums = response.data.response;
            })
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

            @media screen and (max-width: 1200px) {
                & {
                    width: calc(100% / 5 - 1.875rem);
                }
            }

            @media screen and (max-width: 992px) {
                & {
                    width: calc(100% / 4 - 1.875rem);
                }
            }

            @media screen and (max-width: 768px) {
                & {
                    width: calc(100% / 3 - 1.875rem);
                }
            }

            @media screen and (max-width: 576px) {
                & {
                    width: calc(100% / 2 - 1.875rem);
                }
            }

            @media screen and (max-width: 400px) {
                & {
                    width: calc(100% - 1.875rem);
                }
            }
        }
    }
</style>