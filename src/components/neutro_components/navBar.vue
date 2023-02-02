<script>
export default {
    name: 'navBar',
    props: {
        lists: Array,
        headerLogo: String,
        alt: String
    }
}
</script>

<template>
    <nav class="navbar navbar-expand-lg bg-trasparent">
        <div class="container-fluid">
            <a class="navbar-brand" href="#"></a>
            <button class="navbar-toggler justify-content-between" type="button" data-bs-toggle="collapse"
                data-bs-target="#navbarNavDropdown" aria-controls="navbarNavDropdown" aria-expanded="false"
                aria-label="Toggle navigation">
                <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse " id="navbarNavDropdown">
                <ul class="navbar-nav justify-content-between">
                    <li v-for="list in lists" class="nav-item">
                        <a tabindex="0" class="nav-link active selected" aria-current="page" href="#">{{ list }}</a>
                    </li>
                </ul>
            </div>
        </div>
    </nav>
</template>
<!-- <li v-for="list in lists"><a href="">{{ list }}</a></li> -->

<style lang="scss" scoped>
@use '../../assets/scss/partials/variables' as*;



ul {
    list-style-type: none;
    padding: 0;
    margin: 0;
    width: 100%;

    li {
        padding: 5px;
        text-transform: capitalize;
        font-weight: 600;

        a {
            text-shadow: 2px 3px 5px rgba(0, 0, 0, 0.5);
            padding: 5px;
        }
    }


}

.selected {
    border-top: 2px solid transparent;

}

.selected:focus {
    border-top: 2px solid $pm-yellow;
}
</style>