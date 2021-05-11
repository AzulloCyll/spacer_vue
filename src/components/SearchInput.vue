<template>
  <input
    autocomplete="off"
    id="search"
    name="search"
    :value="value"
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
</style>
