<template>
  <div>
    <div>
      <Header />
    </div>
    <div>
      <div class="main">
        <div class="main-left">
          <h1 class="main-title">yes hello hi testing</h1>
          <p class="main-subtitle">
            sed do eiusmod tempor incididunt ut labore
          </p>
        </div>
      </div>
      <div class="timeline-container">
        <div class="timeline">
          <Timeline :data="timeline" />
        </div>
      </div>
    </div>
    <div class="footer">
      <Footer />
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      timeline: [
        {
          pos: "left",
          year: "2019",
          title: "Skypixel",
          subtitle: "when the",
        },
        {
          pos: "right",
          year: "2016",
          title: "Lorem ipsum",
          subtitle: "Lorem ipsum dolor sit amet, consectetur adipisicing elit.",
        },
      ],
    };
  },
};
</script>

<style lang="scss">
body {
  padding: 0;
  margin: 0;
  font-family: "Nunito", sans-serif;
}

.main {
  position: relative;
  overflow: visible;
  z-index: 1;

  &:after {
    content: "";
    width: 100%;
    height: 100%;
    position: absolute;
    background: inherit;
    z-index: -1;
    bottom: 0;
    transform-origin: left bottom;
    transform: skewY(4deg);
  }
  width: 100%;
  height: 85vh;
  display: flex;
  background-color: #feb65e;
  .main-left {
    width: 50%;
    height: 75%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    .main-title {
      width: 50%;
      font-size: 32px;
      font-weight: 500;
      color: #fff;
    }
    .main-subtitle {
      width: 50%;
      font-size: 16px;
      font-weight: 400;
      color: #fff;
    }
  }
}

.timeline-container {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 200%;
  z-index: -1;
  background-color: #363636;
}

.timeline {
  position: absolute;
}
</style>
