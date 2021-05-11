<template>
  <div class="claimWrapper">
    <h1 class="claim">SPACER</h1>
    <p class="subclaim">
      Begin your journey through our amazing galaxy, and discover places you
      never heard of.
    </p>
    <p class="subclaim">Type anything space related to start</p>
  </div>
</template>

<script>
export default {
  name: "Claim",
};
</script>

<style lang="scss" scoped>
.claimWrapper {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  color: white;
}

.claim {
  font-size: 50px;
  margin: 0;
  @media (min-width: 768px) {
    font-size: 80px;
  }
}

.subclaim {
  margin: 20px 0 0 0;
  width: 320px;
  font-size: 13px;
  font-weight: 400;

  @media (min-width: 768px) {
    width: 470px;
    font-size: 17px;
    line-height: 1.5;
    letter-spacing: 1px;
  }
}
</style>
