<template>
  <div class="chip">
    {{ getType(type) }}
  </div>
</template>

<script>
export default {
  props: {
    type: {
      type: Number,
      default: 2,
    },
  },
  methods: {
    getType(type) {
      switch (type) {
        case 0:
          return "Full-time";
        case 1:
          return "Part-time";
        case 2:
          return "Unavailable";
      }
    },
  },
};
</script>

<style scoped lang="scss">
.chip {
  display: inline-block;
  border-radius: 100px;
  padding: 3px 16px;
  background-color: rgba(254, 182, 94, 0.5);
  border: 1px solid rgb(254, 182, 94);
  color: rgb(254, 182, 94);
  font-weight: 600;
  font-size: 12px;
}
</style>
