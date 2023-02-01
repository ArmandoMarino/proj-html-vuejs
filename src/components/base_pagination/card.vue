<script>
export default {
    name: 'card',
    props: {
        title: String,
        class: String,
        text: String,
        image: String,
        alt: String,
        daily: String,
        author: String
    }
}
</script>


<template>
    <div :class="class" class="card p-2">
        <h2>{{ title }}</h2>
        <hr>
        <p>{{ text }}</p>
        <div class="d-flex justify-content-center align-item-center">
            <img :src="image" :alt="alt">
            <p>{{ author }},</p>
            <p :class="class">{{ daily }}</p>
        </div>
    </div>
</template>

<style lang="scss" scoped>

</style>