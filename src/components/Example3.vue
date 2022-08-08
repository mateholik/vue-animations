<template>
  <section>
    <div class="container">
      <div class="content">
        <button @click="exampleThreeShow = !exampleThreeShow">toggle</button>
        <Transition name="bounce">
          <h1 v-show="exampleThreeShow">Example 3</h1>
        </Transition>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      exampleThreeShow: true,
    };
  },
};
</script>

<style>
.bounce-enter-active {
  animation: bounce-in 4s;
}
.bounce-leave-active {
  animation: bounce-in 4s reverse;
}
@keyframes bounce-in {
  0% {
    transform: scale(0);
  }
  50% {
    transform: scale(1.5);
  }
  100% {
    transform: scale(1);
  }
}
</style>
