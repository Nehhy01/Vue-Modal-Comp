<template>
  <div class="backdrop" @click.self="handleClick">
    <div class="modal" :class="{ dark: theme == 'dark', light: theme == 'light' }">
      <slot></slot>
      <slot name="socials"></slot>
      <slot name="links"></slot>
    </div>
  </div>
</template>

<script>
export default {
  name: "Modal",
  props: ["heading", "text", "theme"],
  data() {
    return {};
  },
  methods: {
    handleClick() {
      this.$emit("close");
    },
  },
};
</script>

<style>
.backdrop {
  position: fixed;
  width: 100%;
  height: 100%;
  top: 0;
  left: 0;
  display: flex;
  align-items: start;
  justify-content: center;
  background: rgba(0, 0, 0, 0.5);
}

.modal {
  margin-top: 5rem;
  padding: 2rem;
  background: white;
  color: black;
  border-radius: 5px;
  width: 300px;
}

.modal.dark {
  background: rgb(61, 1, 1);
  color: rgb(216, 216, 216);
}

.modal.light {
  background: rgb(255, 252, 200);
  color: rgb(14, 0, 95);
}
</style>
