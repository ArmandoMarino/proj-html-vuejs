<script>
export default {
    name: 'audioBook'
}
</script>

<template>
    <!-- AGENCYS -->
    <div id="agencys" class="d-flex container justify-content-center align-items-center p-5">
        <img class="img-fluid" src="../../assets/img/main/audiobook/ebay-logotan-2x.png" alt="ebay">
        <img class="img-fluid" src="../../assets/img/main/audiobook/audible-logotan-2x.png" alt="audible">
        <img class="img-fluid" src="../../assets/img/main/audiobook/bb-logotan-2x.png" alt="barnes&noble">
        <img class="img-fluid" src="../../assets/img/main/audiobook/kindlefire-logotan-2x.png" alt="kindle">
    </div>

    <!-- AUDIO-BOOK -->
    <div id="audio-book" class="">
        <div class="container d-flex justify-content-center">
            <img class="app" src="../../assets/img/main/audiobook/audible-app-2x.png" alt="audible">
            <div class="r-audio-book">
                <h3>New Audiobook</h3>
                <h5>NO TIME TO READ? NO PROBLEM. LISTEN TO IT</h5>
                <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit.
                    Obcaecati amet esse consequuntur, ab voluptate est officiis.
                </p>
                <div class="b-audio-book">
                    <img class="img-fluid" src="../../assets/img/main/audiobook/audible-logo.png" alt="audible">
                    <img class="img-fluid" src="../../assets/img/main/audiobook/bn-logo-tall.png" alt="bn">
                    <img class="img-fluid" src="../../assets/img/main/audiobook/kindle-logo-tall.png" alt="kindle">
                </div>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use '../../assets/scss/partials/variables' as *;


#agencys {

    img {
        width: 20%;
        padding: 2rem;
    }
}

.app {
    width: 30%;
}


.r-audio-book {
    flex-basis: 30%;
}
</style>