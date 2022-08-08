<template>
  <section>
    <div class="container">
      <div class="content">
        <button @click="exampleFourShow = !exampleFourShow">toggle</button>
        <Transition
          enter-active-class="animated tada"
          leave-active-class="animated bounceOutRight"
        >
          <h1 v-show="exampleFourShow">Example 4</h1>
        </Transition>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      exampleFourShow: true,
    };
  },
};
</script>

<style></style>
