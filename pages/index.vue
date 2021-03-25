<template>
  <div class="container">
    <div>
      <Logo />
      <h1 class="title">
        Comore
      </h1>
      <h2 class="subtitle">
        {{ getSubtitle() }}
      </h2>
      <div class="links">
        <Link title="Github" logo="https://cdn.como.re/website/github.png" link="https://github.com/ElFamosoComore" />
        <Link title="Comore#0001" logo="https://cdn.como.re/website/discord.png" />
        <Link title="Reddit" logo="https://cdn.como.re/website/reddit.png" link="https://reddit.com/u/ElFamosoComore" />
        <Link title="comore.uno" logo="https://cdn.como.re/website/uno.png" link="https://comore.uno" />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      subtitles: [
        "Créateur de conneries depuis 2005",
        "Glandeur ultime depuis 2005"
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
  color: #2e2e30;
  letter-spacing: 1px;

  -webkit-animation: tracking-in-expand 0.7s cubic-bezier(0.215, 0.610, 0.355, 1.000) both;
	        animation: tracking-in-expand 0.7s cubic-bezier(0.215, 0.610, 0.355, 1.000) both;
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
  color: #526488;
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
</style>
