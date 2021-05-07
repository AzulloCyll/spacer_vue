<template>
  <div class="wrapper">
    <div class="search">
      <label for="search">Search</label>
      <input id="search" name="search" v-model="searchValue" />
    </div>
  </div>
</template>

<script>
export default {
  name: "Search",
  data() {
    return {
      searchValue: "",
    };
  },
};
</script>

<style lang="scss" scoped>

.wrapper {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin: 0;
  padding: 30px;
  width: 100%;
}

.search {
  display: flex;
  flex-direction: column;
  width: 250px;

  label {
    font-family: Lato, sans-serif;
  }

  input {
    height: 50px;
    border: 0;
    border-bottom: 1px solid black;
  }
}
</style>
