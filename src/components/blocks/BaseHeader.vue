<template>
    <header>
        <div class="container">
            <div class="header">
                <LogoSection/>
                <SearchBarSection/>
            </div>
        </div>
    </header>
</template>

<script>
import LogoSection from "../sections/LogoSection.vue";
import SearchBarSection from '../sections/SearchBarSection.vue';

export default {
    name: 'BaseHeader',
    components: {
        LogoSection,
        SearchBarSection
    }
}
</script>

<style lang="scss" scoped>
    header {
        background-color: var(--secondary-color);
        height: var(--header-md);

        .header {
            display: flex;
            align-items: center;
            justify-content: space-between;
        }
    }
</style>