<template>
  <a @click="switchMode">{{ this.$colorMode.value !== "dark" ? "Aller en dark mode" : "Aller en light mode" }}</a>
</template>

<script>
export default {
    methods: {
        switchMode() {
            if(this.$colorMode.value == "light")
                this.$colorMode.preference = "dark"
            else 
                this.$colorMode.preference = "light"
        }
    }
}
</script>