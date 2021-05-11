<template>
    <div class="box">
        <img v-if="this.$colorMode.value != 'dark' || !darkLogo" class="crypto_img" :src='logo' height="24">
        <img v-if="this.$colorMode.value == 'dark' && darkLogo" class="crypto_img" :src='darkLogo' height="24">
        <span><strong>{{ name }}</strong>: {{ wallet }}</span>
    </div>
</template>
<script>
export default {
    props: [
        'name',
        'logo',
        'darkLogo',
        'wallet'
    ]
}
</script>
<style>

.crypto_img {
    margin-right: 5px;
}

.box {
    display: flex;
    flex-wrap: wrap;
    text-align: center;
    justify-content: center;
}
</style>