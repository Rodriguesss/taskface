<template>
  <div>
    <transition name="slide-fade">
      <img v-if="show" src="@/assets/intro.png" width="400" height="400" class="intro" />
    </transition>
  </div>
</template>

<script>
export default {
  data() {
    return {
      show: true,
    };
  },
  mounted() {
    setTimeout(() => {
      this.show = !this.show;
      this.$emit('changedIntro')
    }, 4000);
  },
};
</script>

<style scoped>
.intro {
  position: absolute;
  left: 38%;
  top: 10%;
}

.slide-fade-enter-active {
  transition: all 0.3s ease;
}
.slide-fade-leave-active {
  transition: all 0.8s cubic-bezier(1, 0.5, 0.8, 1);
}
.slide-fade-enter, .slide-fade-leave-to
/* .slide-fade-leave-active em versões anteriores a 2.1.8 */ {
  transform: translateX(10px);
  opacity: 0;
}
</style>