<template>
<div class="update-timer">
  <small class="text-muted">Last updated {{ lastUpdated }}</small>
</div>
</template>

<script>
export default {
  name: 'UpdateTimer',
  props: {
    updateRate: Number,
  },
  data() {
    return {
      timerSeconds: 0,
      lastUpdated: ''
    }
  },
  mounted() {
    this.updateTimer();
  },
  methods: {
    updateTimer() {
      window.setInterval(() => {
        this.timerSeconds++;
        if (this.timerSeconds <= 5) {
          this.lastUpdated = "right now."
        } else {
          this.lastUpdated = this.timerSeconds + " seconds ago";
        }
        if (this.timerSeconds >= this.updateRate) {
          this.timerSeconds = 0;
        }
      }, 1000);
    }
  }
}
</script>

<style src="./css/UpdateTimer.css" scoped>
</style>
