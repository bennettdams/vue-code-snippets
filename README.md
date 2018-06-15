# VUE CODE SNIPPETS

*Curated collection of Vue code snippets/examples/samples for common use cases*

### The goal is to show snippets which are clean (no naming fuzz)
### and vanilla Vue at best


Tired of just another library for a small component you're writing?
The NPM mess is big enough already?

Fear not, let's collect handy Vue code snippets for everybody.

If you want to add your snippet, feel free to send it or create a pull request.

Your submission will be marked with you as the author (if you wish).


# [UTILITY](./utility)

## [Update timer](./utility/update-timer/UpdateTimer.md)

---
> further snippets
---


# EXAMPLES

## [Update timer](./utility/update-timer/UpdateTimer.md)

```html
<template>
<div class="update-timer">
  <small>Last updated {{ lastUpdated }}</small>
</div>
</template>
```

```javascript
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
```
```html
<style src="./css/UpdateTimer.css" scoped>
</style>
```
