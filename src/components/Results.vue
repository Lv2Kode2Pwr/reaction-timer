<template>
  <p>time: {{ scoree }}</p>
  <p class="rank">{{ rank }}</p>
</template>

<script>
export default {
    props: ['scoree'],
    data() {
        return {
            rank: null
        }
    }, 
    mounted() {
        if (this.scoree < 450) {
            this.rank = 'Ninja Fingers'
        } else if (this.scoree < 800) {
            this.rank = 'Rapid Reflexes'
        } else {
            this.rank = 'Snail pace...'
        }
    }
}
</script>

<style>
.rank {
    font-size: 1.4em;
    color: #0faf87;
    font-weight: bold;
}
</style>