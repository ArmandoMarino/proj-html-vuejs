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
        <div class="wrapper text-center">
            <h2>Subscribe to my Newsletter</h2>
            <p>BE NOTIFIED ABOUT BOOK SIGNING YOUR DATES</p>
            <form-email></form-email>
            <span>Lorem ipsum dolor sit amet consectetur adipisicing elit. Molestias, recusandae.</span>
        </div>
    </div>
</template>

<style lang="scss" scoped>
#subscribe {
    min-height: 400px;
    background-image: url(../../assets/img/banner-2.jpg);

    .wrapper {
        color: white;
        width: 50%;
    }
}
</style>