<script>
export default {
    name: 'audioBook'
}
</script>

<template>
    <!-- AGENCYS -------------------->
    <div id="agencys">
        <div class="container-fluid">
            <div class="row p-1 p-md-3  justify-content-center">
                <div class="col-6 col-md-2">
                    <img class="img-fluid" src="../../assets/img/ebay-logotan-2x.png" alt="ebay">
                </div>
                <div class="col-6 col-md-2">
                    <img class="img-fluid" src="../../assets/img/audible-logotan-2x.png" alt="audible">
                </div>
                <div class="col-6 col-md-2">
                    <img class="img-fluid" src="../../assets/img/bb-logotan-2x.png" alt="barnes&noble">
                </div>
                <div class="col-6 col-md-2">
                    <img class="img-fluid" src="../../assets/img/kindlefire-logotan-2x.png" alt="kindle">
                </div>
            </div>
        </div>
    </div>

    <!-- AUDIO-BOOK ------------------->
    <div id="audio-book" class="pt-5">
        <div class="container">
            <div class="row">
                <div class="col-6 d-none d-lg-block ">
                    <!-- LEFT -->
                    <img class="img-fluid" src="../../assets/img/audible-app-2x.png" alt="audible">
                </div>

                <div class="col-12 col-lg-6 d-flex justify-content-center flex-column text-center">
                    <!-- RIGHT -->
                    <div class="r-audio-book ">
                        <h2>New Audiobook</h2>
                        <h6>NO TIME TO READ? NO PROBLEM. LISTEN TO IT</h6>
                        <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit.
                            Obcaecati amet esse consequuntur.
                        </p>
                        <!-- SUB-BOTTOM -->
                        <div class="b-audio-book d-flex justify-content-center">
                            <img class="img-fluid" src="../../assets/img/audible-logo.png" alt="audible">
                            <img class="img-fluid" src="../../assets/img/bn-logo-tall.png" alt="bn">
                            <img class="img-fluid" src="../../assets/img/kindle-logo-tall.png" alt="kindle">
                        </div>
                    </div>
                </div>
            </div>
        </div>

    </div>
</template>

<style lang="scss" scoped>
@use '../../assets/scss/partials/variables' as *;


#agencys {
    background-color: $pm-cream;

    img {
        padding: 1rem;
    }
}

#audio-book {
    color: white;
    background-image: url(../../assets/img/banner.jpg);

    .r-audio-book {
        h6 {
            color: $pm-yellow;
            font-size: 14px;
        }
    }

    .b-audio-book {
        img {
            padding: 10px;
        }
    }
}
</style>