<template>
  <section>
    <div class="container">
      <div class="content">
        <button @click="show = !show">toggle example 7</button>
        <br />
        <Transition name="fading" mode="out-in">
          <button v-if="show" key="save">Save</button>
          <button v-else key="edit">Edit</button>
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
.fading-enter-active,
.fading-leave-active {
  transition: opacity 1s;
}
.fading-enter,
.fading-leave-to {
  opacity: 0;
  /* position: absolute; */
}
.fading-enter-to,
.fading-leave {
  opacity: 1;
}
</style>
