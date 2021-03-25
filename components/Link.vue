<template>
<a
    :href="link"
    target="_blank"
    rel="noopener noreferrer"
    class="button--grey"
>
    <img v-if="this.$colorMode.value != 'dark' || !darkLogo" :src="logo" class="platform_logo" height="32">
    <img v-if="this.$colorMode.value == 'dark' && darkLogo" :src="darkLogo" class="platform_logo" height="32">
    <h5 class="platform_title">{{ title }}</h5>
</a>
</template>

<script>
export default {
    props: ['title', 'logo', 'darkLogo', 'link']
}
</script>

<style>
@-webkit-keyframes swing-in-top-fwd {
  0% {
    -webkit-transform: rotateX(-100deg);
            transform: rotateX(-100deg);
    -webkit-transform-origin: top;
            transform-origin: top;
    opacity: 0;
  }
  100% {
    -webkit-transform: rotateX(0deg);
            transform: rotateX(0deg);
    -webkit-transform-origin: top;
            transform-origin: top;
    opacity: 1;
  }
}
@keyframes swing-in-top-fwd {
  0% {
    -webkit-transform: rotateX(-100deg);
            transform: rotateX(-100deg);
    -webkit-transform-origin: top;
            transform-origin: top;
    opacity: 0;
  }
  100% {
    -webkit-transform: rotateX(0deg);
            transform: rotateX(0deg);
    -webkit-transform-origin: top;
            transform-origin: top;
    opacity: 1;
  }
}

.button--grey {
    -webkit-animation: swing-in-top-fwd 0.5s cubic-bezier(0.175, 0.885, 0.320, 1.275) both;
	        animation: swing-in-top-fwd 0.5s cubic-bezier(0.175, 0.885, 0.320, 1.275) both;
}
</style>