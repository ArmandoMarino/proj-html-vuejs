<script>
import FormEmail from '../neutro_components/FormEmail.vue';
export default {
    name: 'SubscribeSection',
    components: {
        FormEmail
    }
}
</script>

<template>
    <div id="subscribe" class="d-flex justify-content-center align-items-center">
        <div class="container-fluid">
            <div class="row">
                <div class="col-12">
                    <div class="title text-center">
                        <h2>Subscribe to my Newsletter</h2>
                        <p>BE NOTIFIED ABOUT BOOK SIGNING YOUR DATES</p>
                        <form-email></form-email>
                        <span>Lorem ipsum dolor sit amet consectetur adipisicing elit. Molestias, recusandae.</span>
                    </div>
                </div>
            </div>

        </div>

    </div>
</template>

<style lang="scss" scoped>
@use '../../assets/scss/partials/variables' as*;

#subscribe {
    min-height: 400px;
    background-image: url(../../assets/img/banner-2.jpg);
    font-family: 'Newsreader', serif;

    .title>* {
        padding: 5px;
    }

    .title {
        color: white;

        h2 {
            font-weight: 600;
        }

        p {
            font-weight: 600;
            color: $pm-yellow;
        }
    }

}
</style>