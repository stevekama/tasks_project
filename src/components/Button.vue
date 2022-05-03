<template>
  <button 
  @click="onClick()" 
  v-bind:style="{ background: color }" class="btn">
    {{ text }}
  </button>
</template>

<script>
export default {
  name: "Button",
  props: {
    text: {
      type: String,
      default: "Add Task",
      required: true,
    },
    color: {
      type: String,
      default: "green",
      required: true,
    },
  },
  methods: {
    onClick() {
      this.$emit("btn-click");
    },
  },
};
</script>
