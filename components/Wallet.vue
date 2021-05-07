<template>
    <div class="box">
        <img class="crypto_img" :src='logo' height="24">
        <span><strong>{{ name }}</strong>: {{ wallet }}</span>
    </div>
</template>
<script>
export default {
    props: [
        'name',
        'logo',
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