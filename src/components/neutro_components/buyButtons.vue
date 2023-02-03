<script>
export default {
    name: 'buyButtons',
    props: {
        placeHolderLeft: String,
        placeHolderRight: String,
        iconAgencyLeft: String,
        iconAgencyRight: String
    }
}
</script>


<template>
    <!-- BUTTON LEFT -->
    <div class="buy-btn">
        <a href="">
            <i :class="iconAgencyLeft" class="fa-brands"></i>
            {{ placeHolderLeft }}
        </a>
        <span>|</span>
        <a href="">
            <i :class="iconAgencyRight" class="fa-brands"></i>
            {{ placeHolderRight }}
        </a>
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
    color: black;
}

.buy-btn {
    display: flex;
    border-radius: 10px;

    img {
        width: 20px;
    }

}

.buy-btn:hover {
    box-shadow: 0 1px 2px rgba(0, 0, 0, 0.07),
        0 2px 4px rgba(0, 0, 0, 0.07),
        0 4px 8px rgba(0, 0, 0, 0.07),
        0 8px 16px rgba(0, 0, 0, 0.07),
        0 16px 32px rgba(0, 0, 0, 0.07),
        0 32px 64px rgba(0, 0, 0, 0.07);
}
</style>