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
.fade-enter, .fade-leave-to /* .fade-leave-active below version 2.1.8 */ {
  opacity: 0;
}
</style>
