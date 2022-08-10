<template>
  <div class="entry" v-bind="$attrs" v-on="$listeners">
    <div class="entry-title">
      <h1 class="title">{{ entry.title }}</h1>
      <span class="established">est. {{ entry.year }}</span>
    </div>
    <div class="entry-logo">
      <img :src="entry.image" />
    </div>
    <div class="entry-content">
      <p class="description">{{ entry.description }}</p>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    entry: {
      type: Object,
      required: true,
    },
  },
};
</script>

<style scoped lang="scss">
.entry {
  background-color: #404040;
  color: white;
  font-family: "Nunito", sans-serif;
  width: 312px;
  height: 196px;
  border-radius: 8px;
  position: relative;
  transition: all 0.2s ease-in-out;
  top: 0;
  .entry-title {
    position: absolute;
    left: 20px;
    .title {
      font-size: 24px;
      font-weight: 700;
    }
    .established {
      font-size: 12px;
      color: #a3a3a3;
      font-weight: 700;
      margin-top: -16px;
      position: absolute;
    }
  }
  .entry-logo {
    // make it to the right of the title
    position: absolute;
    top: 16px;
    right: -16px;
    width: 100px;
    height: 100px;

    img {
      border-radius: 8px;
      width: 64px;
      height: 64px;
    }
  }
  .entry-content {
    position: absolute;
    left: 20px;
    top: 72px;
    width: 280px;
    height: 100px;
    .description {
      font-size: 14px;
      font-weight: 600;
      color: #a3a3a3;
    }
  }
  &:hover {
    background-color: #4d4d4d;
    top: -6px;
    box-shadow: 0px 4px 12px 0px rgba(0, 0, 0, 0.5);
  }
}
</style>
