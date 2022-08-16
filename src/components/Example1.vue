<template>
  <section>
    <div class="container">
      <div class="content">
        <button @click="show = !show">toggle</button>
        <Transition name="fade">
          <h1 v-show="show">Example 1</h1>
        </Transition>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      show: true,
    };
  },
};
</script>

<style>
.fade-enter-active,
.fade-leave-active {
  transition: opacity 2s;
}
.fade-enter,
.fade-leave-to {
  opacity: 0;
}
.fade-enter-to,
.fade-leave {
  opacity: 1;
}
</style>
