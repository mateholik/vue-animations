<template>
  <section>
    <div class="container">
      <div class="content">
        <button @click="exampleFourShow = !exampleFourShow">toggle</button>
        <Transition
          @beforeEnter="beforeEnter"
          @enter="enter"
          @leave="leave"
          duration="0.5s"
          :css="false"
        >
          <h1 v-show="exampleFourShow">Example 5</h1>
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
  methods: {
    beforeEnter: function (el) {
      el.style.opacity = 0;
      el.style.transformOrigin = "left";
    },
    enter: function (el, done) {
      Velocity(el, { opacity: 1, fontSize: "1.4em" }, { duration: 300 });
      Velocity(el, { fontSize: "1em" }, { complete: done });
    },
    leave: function (el, done) {
      Velocity(el, { translateX: "15px", rotateZ: "50deg" }, { duration: 600 });
      Velocity(el, { rotateZ: "100deg" }, { loop: 2 });
      Velocity(
        el,
        {
          rotateZ: "45deg",
          translateY: "30px",
          translateX: "30px",
          opacity: 0,
        },
        { complete: done }
      );
    },
  },
};
</script>

<style></style>
