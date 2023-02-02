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
                <!-- LEFT -->
                <img class="img-fluid" src="../assets/img/book-widget.png" alt="book-widget">
                <!-- RIGHT -->
                <div class="wrapper">
                    <h4>Latest Book Release</h4>
                    <h6>d. Vaughn autobiography</h6>
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
@use '../assets/scss/partials/variables' as *;

#hero {
    background-image: url(../assets/img/hero-07-2x.jpg);
    background-position: center;
    background-size: cover;
    min-height: 600px;
    padding-top: 150px;
    position: relative;

    // DAILY LEFT SIDE
    .daily {
        width: 500px;
        margin-left: 150px;
        text-shadow: 2px 3px 5px rgba(0, 0, 0, 0.5);
        font-family: 'Newsreader', serif;

        h1 {
            font-family: 'Cedarville Cursive', cursive;
            color: $pm-yellow;
            font-size: 60px;
            margin-bottom: 1rem;
        }

        h3 {
            color: white;
            font-weight: 600;
            font-size: 35px;
        }

        p {
            color: $pm-gray;
            font-style: italic;
            font-size: 20px;
        }
    }

    // LATEST-BOOK RIGHT SIDE
    .latest-book {
        position: absolute;
        right: 0;
        bottom: 0;
        width: 545px;
        min-height: 300px;
        background-color: white;
        padding: 20px;
        font-family: 'Newsreader', serif;

        .wrapper {
            padding: 10px;

            h4 {
                font-weight: 600;
            }

            h6 {
                color: $pm-yellow;
                text-transform: uppercase;
                font-weight: 600;
            }
        }

    }
}
</style>