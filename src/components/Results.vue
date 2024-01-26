<template>
<p>Reaction time: {{score}} milliseconds</p>
<p class="rank">Based on your score your rank is: {{ rank }}</p>
</template>

<script>
export default {
    props: ['score'],
    data() {
        return {
            rank: null
        };
    },
    mounted() {
        if (this.score < 250) {
            this.rank = 'Ninja level'
        }
        else if (this.score < 400 && this.score > 250) {
            this.rank = "Rapid reflexes"
        }
        else {this.rank = "Slowpoke"}
    }
};
</script>

<style>
    .rank {
        font-size: 1.4em;
        color: #0faf87;
        font-weight: bold;
    }
</style>