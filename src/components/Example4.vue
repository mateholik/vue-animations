<template>
  <section>
    <div class="container">
      <div class="content">
        <button @click="show = !show">toggle</button>
        <Transition
          enter-active-class="animated tada"
          leave-active-class="animated fadeOutUpBig"
        >
          <h1 v-show="show">Example 4</h1>
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

<style></style>
