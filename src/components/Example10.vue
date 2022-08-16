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
            class="h-auto overflow-hidden"
            style="transition: height 0.3s ease-out"
            ref="box"
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
  watch: {
    show(newVal) {
      newVal ? this.collapseSection() : this.expandSection();
    },
  },
  methods: {
    expandSection() {
      const item = this.$refs.box;

      item.style.height = item.scrollHeight + "px";

      item.addEventListener("transitionend", () => (item.style.height = null), {
        once: true,
      });
    },
    collapseSection() {
      const item = this.$refs.box;
      const itemTransition = item.style.transition;

      item.style.transition = "";

      requestAnimationFrame(() => {
        item.style.height = item.scrollHeight + "px";
        item.style.transition = itemTransition;
        requestAnimationFrame(() => {
          item.style.height = 0 + "px";
        });
      });
    },
  },
};
</script>

<style></style>
