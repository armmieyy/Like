<template>
  <div>
    <button v-on:click="counter += 1">{{label}}</button>
    <p>{{ counter }}</p>
  </div>
</template>

<script>
export default {
  name: "Button",
  props: {
    label: String,
  },
  data: function () {
    return {
      counter: 0,
      classObject: {
        active: true,
        "text-danger": false,
        weight: 20,
      },
    };
  },
};
</script>

<style>
</style>