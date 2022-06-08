<template>
    <div class="select">
        <label class="select__label" for="typo">Scegli il tuo genere : </label>
        <select class="select__option" name="typo" id="typo">
            <option value="all">All</option>
            <option value="rock">Rock</option>
            <option value="pop">Pop</option>
            <option value="jazz">Jazz</option>
            <option value="metal">Metal</option>
        </select>
    </div>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
.select {
    
    &__label {
        color: var(--primary-color-text);
        text-transform: uppercase;
    }

    &__option {
        padding: .3125rem;
        border-radius: .625rem;
    }
}
</style>