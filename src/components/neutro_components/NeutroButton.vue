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

.btn:hover {
    box-shadow: 0 1px 1px rgba(0, 0, 0, 0.15),
}
</style>