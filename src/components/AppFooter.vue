<script>
import { usefulLinks } from '../data/index.js'
import { contactInfo } from '../data/index.js'

export default {
    name: 'AppFooter',
    data() {
        return {
            usefulLinks,
            contactInfo
        }
    }
}
</script>

<template>
    <footer id="footer" class="p-3">
        <div class="container">
            <div class="row justify-content-center">
                <div class="d-none d-md-block col-3">
                    <img class="img-fluid footer-img" src="../assets/img/author-logo-round.png" alt="#">
                </div>
                <div class="col-4 col-md-3">
                    <h5>ABOUT ME</h5>
                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Nulla facere optio quod, tenetur
                        asperiores animi?</p>
                </div>
                <div class="col-4 col-md-3">
                    <h5>USEFUL LINKS</h5>
                    <ul>
                        <li v-for="usefulLink in usefulLinks"><a href="#">{{ usefulLink }}</a></li>
                    </ul>
                </div>
                <div class="col-4 col-md-3">
                    <h5>CONTACT INFO</h5>
                    <ul>
                        <li v-for="contactInfo in contactInfo"><a href="#">{{ contactInfo }}</a></li>
                    </ul>
                </div>
            </div>
        </div>

    </footer>
</template>

<style lang="scss" scoped>
@use '../assets/scss/partials/variables' as*;

#footer {
    min-height: 300px;
    background-image: url(../assets/img/footer-3.jpg);
    background-size: cover;
    font-family: 'Newsreader', serif;
    color: white;

    p {
        font-size: 14px;
    }

    ul {
        list-style-type: ">";
        margin: 0;
        padding: 0;

        li {
            padding: 5px;

            a {
                padding: 5px 10px;
                text-transform: capitalize;
                font-size: 10px;
            }

            a:hover {
                color: yellow;
            }
        }
    }

    h5 {
        font-size: 15px;
    }

    .footer-img {
        width: 150px;
    }
}
</style>