<template>
    <div class="select">
        <label class="select__label" for="typo">Favourite genre : </label>
        <select class="select__option" name="typo" id="typo" v-model="select.selected">
            <option value="all">All</option>
            <option value="rock">Rock</option>
            <option value="pop">Pop</option>
            <option value="jazz">Jazz</option>
            <option value="metal">Metal</option>
        </select>
    </div>
</template>

<script>
import select from "../../shared/select";

export default {
    name: 'SelectSection',
    data() {
        return {
            select,
        }
    },
}
</script>

<style lang="scss" scoped>
.select {
    
    &__label {
        color: var(--primary-color-text);
        text-transform: uppercase;
        font-size: .9375rem;

        @media screen and (max-width: 25rem){
            & {
                display: none;
            }
        }
    }

    &__option {
        padding: .3125rem;
        border-radius: .625rem;
    }
}
</style>