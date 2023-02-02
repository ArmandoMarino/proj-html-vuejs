<script>
export default {
    name: 'NeutroButton',
    props: {
        label: String,
        href: String,
        class: String
    }
}
</script>

<template>
    <a :href="href || '#'" :class="class" class="btn">{{ label }}</a>
</template>

<style lang="scss" scoped>
a {
    color: white;
    font-size: 12px;
    font-weight: 500;
}
</style>