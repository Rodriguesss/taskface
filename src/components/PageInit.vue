<template>
  <div class="initial">
    <span><div>Bem vindo {{ name }}</div></span>
    <CardList />
  </div>

</template>

<script>
import CardList from "@/components/CardList.vue";
export default {
  components: {
    CardList
  },
  props: {
    name: String,
  },
};
</script>

<style scoped>

</style>