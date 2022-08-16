<template>
  <section>
    <div class="container">
      <div class="content">
        <button v-on:click="shuffle">Shuffle example 6</button>
        <button v-on:click="add">Add</button>
        <button v-on:click="remove">Remove</button>
        <transition-group name="random" tag="p">
          <span v-for="item in items" v-bind:key="item" class="random-item">
            {{ item }}
          </span>
        </transition-group>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      items: [1, 2, 3, 4, 5, 6, 7, 8, 9],
      nextNum: 10,
    };
  },
  methods: {
    randomIndex: function () {
      return Math.floor(Math.random() * this.items.length);
    },
    add: function () {
      this.items.splice(this.randomIndex(), 0, this.nextNum++);
    },
    remove: function () {
      this.items.splice(this.randomIndex(), 1);
    },
    shuffle: function () {
      this.items = _.shuffle(this.items);
    },
  },
};
</script>

<style>
.random-item {
  transition: all 1s;
  display: inline-block;
  margin-right: 10px;
}
.random-enter,
.random-leave-to {
  opacity: 0;
  transform: translateY(30px);
}
.random-leave-active {
  position: absolute;
}
</style>
