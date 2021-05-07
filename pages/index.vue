<template>
  <div class="container">
    <div>
      <Logo />
      <h1 class="title">
        Comore
      </h1>
      <div class="links">
        <Link title="Github" logo="https://cdn.como.re/website/light/github.png" darkLogo="https://cdn.como.re/website/dark/github.png" link="https://github.com/ElFamosoComore" />
        <Link title="Comore#0001" logo="https://cdn.como.re/website/light/discord.png" darkLogo="https://cdn.como.re/website/dark/discord.png" />
        <Link title="Reddit" logo="https://cdn.como.re/website/light/reddit.png" link="https://reddit.com/u/ElFamosoComore" />
        <Link title="comore.uno" logo="https://cdn.como.re/website/light/uno.png" darkLogo="https://cdn.como.re/website/dark/uno.png" link="https://comore.uno" />
      </div>
      <div class="wallets">
        <Wallet name="Bitcoin" wallet="bc1q6fqf72n3nydqh30qmfw54cmyu5jlxg7gzevhwd" logo="https://en.bitcoin.it/w/images/en/2/29/BC_Logo_.png" />
        <Wallet name="Bitcoin Cash" wallet="qrthyyap23wypf7dydwqqh2j97zyuzw0zg33ez55tt" logo="https://upload.wikimedia.org/wikipedia/commons/5/58/Bitcoin_Cash.png" />
      </div>
    </div>

    <ModeToggleButton class="mode-switcher" v-bind:checked="this.$colorMode.value" />
  </div>
</template>

<script>
export default {
  data() {
    return {
      subtitles: [
      ]
    }
  },
  methods: {
    getSubtitle() {
      return this.subtitles[Math.floor(Math.random() * this.subtitles.length)];
    }
  }
}
</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

a:-webkit-any-link{
  text-decoration:none !important;
}

.title {
  font-family:
    'Quicksand',
    'Source Sans Pro',
    -apple-system,
    BlinkMacSystemFont,
    'Segoe UI',
    Roboto,
    'Helvetica Neue',
    Arial,
    sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: var(--color-primary);
  letter-spacing: 1px;
  padding-bottom: 0.40em;

  -webkit-animation: tracking-in-expand 0.7s cubic-bezier(0.215, 0.610, 0.355, 1.000) both;
	        animation: tracking-in-expand 0.7s cubic-bezier(0.215, 0.610, 0.355, 1.000) both;
}

.wallets {
  -webkit-animation: flip-in-hor-bottom 0.5s cubic-bezier(0.250, 0.460, 0.450, 0.940) both;
	        animation: flip-in-hor-bottom 0.5s cubic-bezier(0.250, 0.460, 0.450, 0.940) both;
}

.mode-switcher {
  position: absolute; 
  bottom: 0; 
  width: 50%; 
  padding-bottom: 0.75em;
}

@-webkit-keyframes tracking-in-expand {
  0% {
    letter-spacing: -0.5em;
    opacity: 0;
  }
  40% {
    opacity: 0.6;
  }
  100% {
    opacity: 1;
  }
}
@keyframes tracking-in-expand {
  0% {
    letter-spacing: -0.5em;
    opacity: 0;
  }
  40% {
    opacity: 0.6;
  }
  100% {
    opacity: 1;
  }
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: var(--color-secondary);
  word-spacing: 5px;
  padding-bottom: 15px;
  font-style: italic;
  -webkit-animation: tilt-in-bottom-2 0.6s cubic-bezier(0.250, 0.460, 0.450, 0.940) both;
	        animation: tilt-in-bottom-2 0.6s cubic-bezier(0.250, 0.460, 0.450, 0.940) both;
}

@-webkit-keyframes tilt-in-bottom-2 {
  0% {
    -webkit-transform: rotateY(-30deg) translateY(300px) skewY(30deg);
            transform: rotateY(-30deg) translateY(300px) skewY(30deg);
    opacity: 0;
  }
  100% {
    -webkit-transform: rotateY(0deg) translateY(0) skewY(0deg);
            transform: rotateY(0deg) translateY(0) skewY(0deg);
    opacity: 1;
  }
}
@keyframes tilt-in-bottom-2 {
  0% {
    -webkit-transform: rotateY(-30deg) translateY(300px) skewY(30deg);
            transform: rotateY(-30deg) translateY(300px) skewY(30deg);
    opacity: 0;
  }
  100% {
    -webkit-transform: rotateY(0deg) translateY(0) skewY(0deg);
            transform: rotateY(0deg) translateY(0) skewY(0deg);
    opacity: 1;
  }
}
@-webkit-keyframes flip-in-hor-bottom {
  0% {
    -webkit-transform: rotateX(80deg);
            transform: rotateX(80deg);
    opacity: 0;
  }
  100% {
    -webkit-transform: rotateX(0);
            transform: rotateX(0);
    opacity: 1;
  }
}
@keyframes flip-in-hor-bottom {
  0% {
    -webkit-transform: rotateX(80deg);
            transform: rotateX(80deg);
    opacity: 0;
  }
  100% {
    -webkit-transform: rotateX(0);
            transform: rotateX(0);
    opacity: 1;
  }
}
</style>
