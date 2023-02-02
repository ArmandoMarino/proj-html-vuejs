<script>
export default {
    name: 'FormEmail'
}
</script>

<template>
    <form>
        <input placeholder="Insert your email..." type="email" id="email" name="email">
        <input class="my-subscribe" type="submit" value="Subscribe">
    </form>
</template>

<style lang="scss" scoped>
@use '../../assets/scss/partials/variables' as *;

.my-subscribe {
    padding: 2px 10px;
    background-color: $pm-green;
}
</style>