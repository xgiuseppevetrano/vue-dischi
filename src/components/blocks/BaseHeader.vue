<template>
    <header>
        <div class="container">
            <LogoSection/>
        </div>
    </header>
</template>

<script>
import LogoSection from "../sections/LogoSection.vue";

export default {
    name: 'BaseHeader',
    components: {
        LogoSection
    }
}
</script>

<style lang="scss" scoped>
    header {
        background-color: var(--secondary-color);
        height: var(--header-md);

        .container {
            margin: 0;
        }
    }
</style>