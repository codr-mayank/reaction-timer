<template>
  <p>Reaction Time: {{ score }} ms</p>
  <p class="remark">Remarks: {{ remark }}</p>
</template>

<script>
export default {
  name: 'Results',
  props: {
    score: Number
  },
  data() {
    return {
      remark: null
    }
  },
  mounted() {
    if (this.score < 250) {
      this.remark = 'Ninja Fingers';
    } else if (this.score < 400) {
      this.remark = 'Rapid Reflexes';
    } else {
      this.remark = 'Snail pace ... :(';
    }
  }
}
</script>

<style>
  .remark {
    font-size: 1.4em;
    color: #0faf87;
    font-weight: bold;
  }
</style>