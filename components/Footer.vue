<template>
  <div class="footer">
    <div class="footer-left">
      <div class="footer-icon">
        <img draggable="false" src="/img/logo.png" alt="" />
      </div>
      <span>Bloxite | something will go here eventually</span>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped lang="scss">
.footer {
  position: fixed;
  bottom: 0;
  z-index: 99999;
  background-color: #222222;
  width: 100%;
  height: 100px;
  .footer-icon {
    img {
      filter: grayscale(100%);
      width: 64px;
      height: 64px;
      margin: 16px;
    }
  }

  span {
    color: #5a5a5a;
    font-size: 16px;
    margin: -100px;
  }
}
</style>
