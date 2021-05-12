<template>
  <div class="hello">
    <transition
      name="custom-classes-transition"
      leave-active-class="animated bounceOutRight"
    >
      <div v-if="show">
        <img
          alt="TaskFace logo"
          src="@/assets/task_face.gif"
          class="logo-initial"
          width="400"
          height="400"
        />

        <div class="form-input-initial">
          <p class="title-input">Qual o seu nome?</p>
          <input
            v-model="name"
            @keydown.enter="init"
            type="text"
            class="form-element"
            placeholder="João..."
          />
          <button class="form-element" @click="init">+</button>
        </div>
      </div>
    </transition>
  </div>
</template>
<script>
export default {
  data() {
    return {
      name: "",
      show: true,
    };
  },
  methods: {
    init() {
      this.show = !this.show;
      setTimeout(() => {
        this.$emit('changedPageInitial', this.name)
      }, 700);
    },
  },
};
</script>

<style scoped>
@import url("https://cdn.jsdelivr.net/npm/animate.css@3.5.1");
@import url("https://fonts.googleapis.com/css2?family=Raleway:wght@100&display=swap");

.new-task {
  margin: 35px;
}

.form-input-initial {
  margin-top: -25px;
}

.form-element {
  outline: none;
  font-size: 2rem;
  border: 1px solid #fff;
  padding: 5px 10px 8px;
  color: #000;
  font-family: "Raleway", sans-serif;
  font-size: 1.5em;
  font-weight: 300;
}

.title-input {
  font-family: "Raleway", sans-serif;
  font-size: 1.4em;
  font-weight: 600;
}

.logo-initial {
  margin-top: -80px;
}

input.form-element {
  width: 500px;
  background-color: #fff2;
  border-top-left-radius: 8px;
  border-bottom-left-radius: 8px;
  border: 1px solid rgb(197, 195, 195);
}

input.form-element:hover {
  border: 1px solid rgb(102, 102, 102);
  transition: border 1s;
}

button.form-element {
  cursor: pointer;
  border-left: none;
  background-color: #333536;
  border-top-right-radius: 5px;
  border-bottom-right-radius: 5px;
  color: #fff;
  font-size: 1.6em;
  padding-bottom: 9px;
}

button.form-element:hover {
  background-color: #202122;
}
</style>
