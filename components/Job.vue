<template>
  <div class="job" v-bind="$attrs" v-on="$listeners">
    <div class="job-top">
      <img class="job-banner" :src="job.banner" />
    </div>
    <div class="job-content">
      <span class="job-name">{{ job.name }}</span>
      <JobTypeChip :type="job.type" />
    </div>
    <div class="job-description">
      <span class="job-description-text">{{ job.description }}</span>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    job: {
      type: Object,
      default: () => ({}),
    },
  },
};
</script>

<style scoped lang="scss">
.job {
  margin: 16px;
  width: 256px;
  height: 256px;
  box-shadow: 0px 2px 4px rgba(0, 0, 0, 0.25);
  border-radius: 8px;
  .job-banner {
    width: 100%;
    border-radius: 8px 8px 0 0;
  }
  .job-content {
    margin-left: 8px;
    display: inline-block;
    .job-name {
      display: inline-block;
      font-size: 16px;
      font-weight: 700;
    }
  }
  .job-description {
    margin-left: 8px;
    margin-right: 8px;
    display: inline-block;
    .job-description-text {
      display: inline-block;
      font-size: 14px;
      font-weight: 500;
      color: #8c8c8c;
    }
  }
}
</style>
