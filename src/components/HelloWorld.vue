<script setup lang="ts">
defineProps<{
  msg: string
}>()
</script>

<template>
  <div class="greetings">
    <h1 @mouseenter="$emit('hover')" class="green">{{ msg }}</h1>
    <h3>
      Mening to'liq ismim <span class="green">Raxmatulloyev Shukrullojon</span>. 2019-yili TATU
      Samarqand filialiga o'qishga kirib, dasturlash sohasini o'rganib kelyapman.
    </h3>
  </div>
</template>

<style scoped>
h1 {
  font-weight: 500;
  font-size: 2.6rem;
  position: relative;
  top: -10px;
}

h3 {
  font-size: 1.2rem;
}

.greetings h1,
.greetings h3 {
  text-align: center;
}

@media (min-width: 1200px) {
  .greetings h1,
  .greetings h3 {
    text-align: left;
  }
}
</style>
