<template>
  <div>
    <div class="container" :style="'background-color:' + bgColor">
      <div class="left">
        <img
          class="logo"
          src="/img/logo.png"
          alt="logo"
          width="48"
          height="48"
        />
      </div>
      <div class="right">
        <div class="items">
          <nuxt-link
            class="item"
            :style="'color:' + color"
            :class="{ 'item-bold': $route.path === '/' }"
            to="/"
          >
            Home
          </nuxt-link>
          <nuxt-link
            class="item"
            :style="'color:' + color"
            :class="{ 'item-bold': $route.path === '/careers' }"
            to="/careers"
          >
            Apply
          </nuxt-link>
          <a class="item" :style="'color:' + color" href="#"> Discord </a>
          <nuxt-link
            class="item"
            :style="'color:' + color"
            :class="{ 'item-bold': $route.path === '/contact' }"
            to="/contact"
          >
            Contact
          </nuxt-link>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    bgColor: {
      type: String,
      default: "#feb65e",
    },
    color: {
      type: String,
      default: "#fff",
    },
  },
};
</script>

<style scoped lang="scss">
.container {
  width: 100%;
  height: 76px;
  top: 0;
  position: relative;
  transition: 0.3s ease-in-out;
  z-index: 99999;
  &:hover {
    box-shadow: 0px 2px 4px rgba(0, 0, 0, 0.25);
  }
}

.left {
  .logo {
    display: block;
  }
  position: absolute;
  top: 50%;
  left: 16px;
  transform: translateY(-50%);
}

.right {
  position: absolute;
  top: 50%;
  right: 24px;
  transform: translateY(-50%);
  .items {
    display: flex;
    align-items: center;
    .item {
      font-weight: 500;
      margin-left: 16px;
      font-size: 17px;
      text-decoration: none;
      &:first-child {
        margin-left: 0;
      }
    }
    .item-bold {
      font-weight: 700;
    }
  }
}
</style>
