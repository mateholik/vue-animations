<template>
  <section>
    <div class="container">
      <div class="content">
        <button @click="show = !show">toggle example 10</button>
        <div class="max-w-md">
          <div class="border-4 border-solid border-green-300 p-4">
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Inventore
            suscipit quod exercitationem quisquam sed perspiciatis deleniti
            pariatur reprehenderit est sunt.
          </div>

          <div
            class="h-auto overflow-hidden duration-500"
            ref="box"
            :style="`height: ${height}`"
          >
            <p class="p-4 border-4 border-solid border-red-300">
              Lorem ipsum dolor sit amet consectetur, adipisicing elit. Maiores
              blanditiis quo doloribus consequuntur quae iure pariatur modi
              aperiam, cupiditate porro. Inventore asperiores accusamus tempora
              necessitatibus sint dolores deleniti eum. Molestias, ipsa
              repellendus explicabo soluta quos odio sapiente adipisci qui.
              Animi.
            </p>
          </div>

          <div class="border-4 border-solid border-blue-300 p-4">
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Libero,
            non!
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      show: false,
    };
  },
  computed: {
    height() {
      return this.show ? this.$refs.box.clientHeight + "px" : 0;
    },
  },
  methods: {
    expandSection() {
      this.$refs.box.style.height = this.$refs.box.clientHeight + "px";
    },
    collapseSection() {
      // get the height of the element's inner content, regardless of its actual size
      var sectionHeight = this.$refs.box.clientHeight;

      // temporarily disable all css transitions
      var elementTransition = element.style.transition;
      this.$refs.box.style.transition = "";

      // on the next frame (as soon as the previous style change has taken effect),
      // explicitly set the element's height to its current pixel height, so we
      // aren't transitioning out of 'auto'
      requestAnimationFrame(function () {
        sectionHeight.style.height = sectionHeight + "px";
        sectionHeight.style.transition = elementTransition;

        // on the next frame (as soon as the previous style change has taken effect),
        // have the element transition to height: 0
        requestAnimationFrame(function () {
          sectionHeight.style.height = 0 + "px";
        });
      });
    },
  },
};
</script>

<style></style>
