<template>
  <div class="initial">Bem vindo {{ name }}</div>
</template>

<script>
export default {
  props: {
    name: String,
  },
};
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Yellowtail&display=swap');

.initial {
  font-family: 'Yellowtail', cursive;
  font-size: 2.5em;
}


</style>