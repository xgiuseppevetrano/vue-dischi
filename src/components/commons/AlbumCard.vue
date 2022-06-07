<template>
    <div class="album">
        <img class="album__img" :src="album.poster" :alt="album.title">
        <h5 class="album__title">{{album.title}}</h5>
        <span class="album__author">{{album.author}}</span>
        <small class="album__year">{{album.year}}</small>
    </div>
</template>

<script>
export default {
    name: 'AlbumCard',
    props: {
        album: Object,
    }
}
</script>

<style lang="scss" scoped>
    .album {
        background-color: var(--secondary-color);
        color: var(--secondary-color-text);
        padding: .625rem;
        text-align: center;

        &__img {
            width: 100%;
            aspect-ratio: 1;
        }

        &__title {
            color: var(--primary-color-text);
            text-transform: uppercase;
            margin: .625rem 0;
        }

        &__author {
            display: block;
        }
    }
</style>