<template>
    <div class="search-bar">
        <input class="search-bar__input" type="text" placeholder="Search artist" v-model="select.text">
    </div>
</template>

<script>
import select from "../../shared/select";

export default {
    name: 'SearchBarSection',
    data() {
        return {
            select,
        }
    },
}
</script>

<style lang="scss" scoped>
    .search-bar__input {
        padding: .3125rem;
        border-radius: .625rem;
        border: .0625rem solid var(--secondary-color);
        text-align: center;
    }
</style>