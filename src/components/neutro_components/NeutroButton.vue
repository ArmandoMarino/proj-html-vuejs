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
    box-shadow: 0 1px 2px rgba(0, 0, 0, 0.07),
        0 2px 4px rgba(0, 0, 0, 0.07),
        0 4px 8px rgba(0, 0, 0, 0.07),
        0 8px 16px rgba(0, 0, 0, 0.07),
        0 16px 32px rgba(0, 0, 0, 0.07),
        0 32px 64px rgba(0, 0, 0, 0.07);
}
</style>