<template>
  <section>
    <div class="container">
      <div class="content">
        <button @click="show = !show">toggle example 11</button>
        <div class="max-w-md flex flex-col" style="height: 600px">
          <div class="flex-1 overflow-hidden">
            <p class="border-4 border-solid border-green-300 p-4 h-full">
              Lorem ipsum dolor sit amet consectetur adipisicing elit. Inventore
              suscipit quod exercitationem quisquam sed perspiciatis deleniti
              pariatur reprehenderit est sunt.
            </p>
          </div>

          <div
            class="overflow-hidden duration-500"
            :style="show ? 'flex: 1' : 'flex: 0'"
          >
            <p class="p-4 border-4 border-solid border-red-300 h-full">
              Lorem, ipsum dolor sit amet consectetur adipisicing elit. Iure
              voluptate ad est debitis sed beatae optio quasi, cupiditate facere
            </p>
          </div>

          <div class="flex-1 overflow-hidden">
            <p class="border-4 border-solid border-blue-300 p-4 h-full">
              Lorem ipsum dolor sit amet consectetur adipisicing elit. Libero,
              non!
            </p>
          </div>
        </div>
        <!-- <div class="flex flex-col text-2xl" style="height: 300px">
          <div class="flex-1 bg-red-200 overflow-hidden">
            <p>
              Lorem ipsum dolor sit amet consectetur adipisicing elit. Ab,
              assumenda?
            </p>
          </div>
          <div
            class="flex-1 bg-green-200 overflow-hidden transition-all duration-500"
            :style="show ? 'flex: 1' : 'flex: 0'"
          >
            Lorem, ipsum dolor sit amet consectetur adipisicing elit.
            Consequatur aut est cumque modi minima! Repellendus esse provident
            molestias soluta quo.
          </div>
          <div class="flex-1 bg-blue-200 overflow-hidden">
            Lorem ipsum dolor sit amet, consectetur adipisicing elit.
            Repudiandae recusandae delectus quibusdam mollitia ad dolore
            corrupti, praesentium maiores ipsa laboriosam qui explicabo aperiam
            fugiat quis reprehenderit at! Ducimus, itaque commodi!
          </div>
        </div> -->
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
