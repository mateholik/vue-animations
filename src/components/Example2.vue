<template>
  <section>
    <div class="container">
      <div class="content">
        <button @click="exampleTwoShow = !exampleTwoShow">toggle</button>
        <Transition name="slide-fade">
          <h1 v-show="exampleTwoShow">Example 2</h1>
        </Transition>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      exampleTwoShow: true,
    };
  },
};
</script>

<style>
.slide-fade-enter-active {
  transition: all 0.3s ease;
}
.slide-fade-leave-active {
  transition: all 0.8s cubic-bezier(1, 0.5, 0.8, 1);
}
.slide-fade-enter,
.slide-fade-leave-to {
  transform: translateX(10px);
  opacity: 0;
}
</style>
