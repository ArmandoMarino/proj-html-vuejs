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
    <div class="buy-btn">
        <button class="buy-btn-l" name="buy-button" type="submit">
            <span>{{ imageAgencyLeft }}</span>
            {{ placeHolderLeft }}
        </button>
        <!-- BUTTON RIGHT -->
        <button class="buy-btn-r" name="buy-button" type="submit">
            {{ placeHolderRight }}
        </button>
    </div>

</template>

<style lang="scss" scoped>
@use '../../assets/scss/partials/variables' as *;

.wrapper {
    font-weight: 700;
}

.buy-btn>* {
    background-color: #f5fcfa;
    border-radius: 5px;
    font-size: 15px;
    padding: 5px;
}

.buy-btn {
    display: flex;

    img {
        width: 20px;
    }

}
</style>