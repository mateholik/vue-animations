<template>
  <section>
    <div class="container">
      <div class="content">
        <button @click="exampleFiveShow = !exampleFiveShow">toggle</button>
        <br />
        <Transition name="fade" mode="out-in">
          <button v-if="exampleFiveShow" key="save">Save</button>
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
      exampleFiveShow: true,
    };
  },
};
</script>

<style></style>
