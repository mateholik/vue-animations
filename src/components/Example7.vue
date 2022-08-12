<template>
  <section>
    <div class="container">
      <div class="content">
        <button @click="show = !show">toggle example 7</button>
        <br />
        <Transition name="fade" mode="out-in">
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

<style></style>
