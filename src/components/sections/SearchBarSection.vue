<template>
    <div class="select">
        <label class="select__label" for="typo">Scegli il tuo genere : </label>
        <select class="select__option" name="typo" id="typo" v-model="select.selected">
            <option value="All">All</option>
            <option value="Rock">Rock</option>
            <option value="Pop">Pop</option>
            <option value="Jazz">Jazz</option>
            <option value="Metal">Metal</option>
        </select>
    </div>
</template>

<script>
import select from "../../shared/select";

export default {
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
    }

    &__option {
        padding: .3125rem;
        border-radius: .625rem;
    }
}
</style>