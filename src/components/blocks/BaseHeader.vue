<template>
  <header>
      <LogoSection class="p-2"/>
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
    }
</style>