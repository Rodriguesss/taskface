<template>
  <div class="card-container">
    <div class="card-body">
      <p>
        Task
      </p>
    </div>
  </div>
</template>
<script>
export default {
  name: "Card",
};
</script>
<style scoped>
.card-container {
  position: relative;
  box-sizing: border-box;
  padding: 10px;
  border-radius: 8px;
  font-size: 2rem;
  font-weight: 300;
  user-select: none;
  display: flex;
  justify-content: center;
  align-items: center;
  background: #FFF952;
  box-shadow: 0px 2px 10px rgba(0, 0, 0, 0.15);
  width: 100%;
  height: 100%;
  cursor: pointer;
  margin-bottom: 2rem;
}
.card-body {
  padding: 1rem 2rem;
}
p {
  font-size: 1.6rem;
}
</style>