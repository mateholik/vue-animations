<template>
  <section>
    <div class="container">
      <div class="content">
        <button @click="show = !show">toggle example 9</button>
        <div class="max-w-md">
          <div class="border-4 border-solid border-green-300 p-4">
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Inventore
            suscipit quod exercitationem quisquam sed perspiciatis deleniti
            pariatur reprehenderit est sunt.
          </div>

          <div
            class="transform origin-top h-auto overflow-hidden duration-500"
            :class="show ? 'scale-y-100' : 'scale-y-0'"
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
      show: true,
    };
  },
};
</script>

<style></style>
