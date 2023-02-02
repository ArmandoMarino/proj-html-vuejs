<script>
import buyButtons from './neutro_components/buyButtons.vue';
export default {
    name: 'AppHero',
    components: {
        buyButtons
    }
}
</script>

<template>
    <section id="hero" class="">
        <!-- DAILY REVIEW -->
        <div class="daily ">
            <h1>Damon Vaughn</h1>
            <h3>Best-selling author and the most
                influential public intellectual in the
                western world right now.
            </h3>
            <p>-The New York Times</p>
        </div>

        <!-- LATEST-BOOK -->
        <div class="latest-book ">
            <div class="t-latest-book d-flex">
                <img class="img-fluid" src="../assets/img/book-widget.png" alt="book-widget">
                <div class="wrapper">
                    <h4>Latest Book Release</h4>
                    <p>d. Vaughn autobiography</p>
                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.
                        Odio illo quidem fugit pariatur provident cupiditate sint quam
                        consequatur numquam nam?
                    </p>
                </div>
            </div>
            <div class="d-flex justify-content-center">
                <buy-buttons :placeHolderLeft="'Buy on Amazon'" :placeHolderRight="'Buy on Apple Store'"
                    :imageAgencyLeft="`\e90a`"></buy-buttons>
            </div>

        </div>
    </section>
</template>

<style lang="scss" scoped>
#hero {
    background-image: url(../assets/img/hero-07-2x.jpg);
    background-position: center;
    background-size: cover;
    min-height: 500px;
    padding-top: 150px;
    position: relative;

    .daily {
        width: 500px;
        margin-left: 150px;
    }

    .latest-book {
        position: absolute;
        width: 30%;
        right: 0;
        bottom: 0;
        width: 600px;
        background-color: white;
        padding: 20px;

        .wrapper {
            padding: 10px;
        }

    }
}
</style>