<template>
  <div>
    <div>
      <Header bg-color="white" color="black" />
    </div>
    <div>
      <div class="title-top">
        <h1 class="title">Jobs</h1>
      </div>
      <div class="main-content">
        <div class="jobs">
          <Job v-for="job in jobs" v-bind:key="job.id" :job="job" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      jobs: [
        {
          name: "PMMP Developer",
          type: 0,
          id: 0,
          description: "somebody who has way more patience than me",
          banner: "https://kappug.dev/i/banner_AmongUs.jpg",
        },
        {
          name: "PMMP Developer",
          type: 0,
          id: 0,
          description: "somebody who has way more patience than me",
          banner: "https://kappug.dev/i/banner_AmongUs.jpg",
        },
        {
          name: "PMMP Developer",
          type: 0,
          id: 0,
          description: "somebody who has way more patience than me",
          banner: "https://kappug.dev/i/banner_AmongUs.jpg",
        },
        {
          name: "PMMP Developer",
          type: 0,
          id: 0,
          description: "somebody who has way more patience than me",
          banner: "https://kappug.dev/i/banner_AmongUs.jpg",
        },
      ],
    };
  },
};
</script>

<style scoped lang="scss">
.title-top {
  width: 100%;
  height: 128px;
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: #feb65e;
  .title {
    color: white;
    font-size: 32px;
    font-weight: 700;
  }
  animation: fadeIn 0.2s ease-in-out;
}

.jobs {
  // make 2 jobs on the same row
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  align-items: center;
  width: 100%;
  animation: fadeIn 0.2s ease-in-out;
}

@keyframes fadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}
</style>
