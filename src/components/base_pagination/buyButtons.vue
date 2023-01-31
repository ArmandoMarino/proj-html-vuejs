<script>
export default {
    name: 'buyButtons',
    props: {
        placeHolderLeft: String,
        placeHolderRight: String,
        imageAgencyLeft: String,
        imageAgencyRight: String
    }
}
</script>


<template>
    <!-- BUTTON LEFT -->
    <button class="buy-btn-l" name="buy-button" type="submit">
        <span>{{ imageAgencyLeft }}</span>
        {{ placeHolderLeft }}
    </button>
    <!-- BUTTON RIGHT -->
    <button class="buy-btn-r" name="buy-button" type="submit">
        {{ placeHolderRight }}
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