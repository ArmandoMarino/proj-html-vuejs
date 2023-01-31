<script>
export default {
    name: 'buyButton',
    props: {
        placeholder: String,
        imageAgency: String
    }
}
</script>


<template>
    <!-- BUTTON ONE -->
    <button class="buy-btn" name="buy-button" type="submit">
        <img :src="imageAgency" :alt="placeholder">
        {{ placeholder }}
    </button>
    <!-- BUTTON TWO -->
    <button class="buy-btn" name="buy-button" type="submit">
        <img :src="imageAgency" :alt="placeholder">
        {{ placeholder }}
    </button>
</template>

<style lang="scss" scoped>
.buy-btn {
    display: flex;

    img {
        width: 20px;
    }
}
</style>