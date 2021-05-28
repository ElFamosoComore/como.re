<template>
  <div>
  <img v-if="this.$colorMode.value == 'dark'" class="logo" src="https://cdn.como.re/website/dark/logo.svg" width="245" height="180">
  <img v-else class="logo" src="https://cdn.como.re/website/light/logo.svg" width="245" height="180">
  </div>
</template>

<style>
.logo {
  -webkit-animation: scale-in-center 0.5s cubic-bezier(0.250, 0.460, 0.450, 0.940) both;
	        animation: scale-in-center 0.5s cubic-bezier(0.250, 0.460, 0.450, 0.940) both;
  margin: auto;
}

@-webkit-keyframes scale-in-center {
  0% {
    -webkit-transform: scale(0);
            transform: scale(0);
    opacity: 1;
  }
  100% {
    -webkit-transform: scale(1);
            transform: scale(1);
    opacity: 1;
  }
}
@keyframes scale-in-center {
  0% {
    -webkit-transform: scale(0);
            transform: scale(0);
    opacity: 1;
  }
  100% {
    -webkit-transform: scale(1);
            transform: scale(1);
    opacity: 1;
  }
}

</style>
