<template>
  <div>
    <Nuxt />
  </div>
</template>

<style>
*,
*::before,
*::after {
  box-sizing: border-box;
  margin: 0;
}
.button--grey {
  display: inline-block;
  color: var(--color-primary);
  text-decoration: none;
  padding: 10px 30px;
  margin-left: 15px;
}

body {
  background-color: #fff;
  color: rgba(0,0,0,0.8);
}
.dark-mode body {
  background-color: #091a28;
  color: #ebf4f1;
}
.sepia-mode body {
  background-color: #f1e7d0;
  color: #433422;
}
</style>
