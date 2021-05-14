<template>
  <input
    autocomplete="off"
    id="search"
    name="search"
    :value="value"
    :class="{ dark: dark }"
    @input="handleChange"
  />
</template>

<script>
export default {
  name: "SearchInput",
  props: {
    value: {
      type: String,
      required: true,
    },
    dark: {
      type: Boolean,
      default: false,
    },
  },
  methods: {
    handleChange(e) {
      this.$emit("input", e.target.value);
    },
  },
};
</script>
<style lang="scss" scoped>
input {
  color: white;
  text-align: center;
  font-size: 18px;
  height: 30px;
  font-weight: 300;
  border: 0;
  background: none;
  border-bottom: 1px solid white;
  transition: box-shadow 0.3s ease-out;
  margin-top: 50px;
}

input:focus {
  outline: none;
  box-shadow: 0 10px 20px -8px rgba(255, 255, 255, 0.3);
}

.dark {
  color: #1e3d4a;
  border-bottom-color: #1e3d4a;
}

.dark:focus {
  outline: none;
  box-shadow: 0 10px 20px -8px rgba(#1e3d4a, 0.3);
}
</style>
