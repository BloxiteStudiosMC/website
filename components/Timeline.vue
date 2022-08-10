<template>
  <div>
    <div class="line"></div>
    <div class="left-events">
      <div class="left-event">
        <TimelineEntry :entry="entries.skypixel" />
      </div>
    </div>
    <div class="right-events">
      <div class="right-event">
        <TimelineEntry :entry="entries.bloxite" />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      entries: {
        skypixel: {
          title: "Skypixel",
          year: "2019",
          description:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor",
          image: "https://kappug.dev/i/kitten.jpg",
        },
        bloxite: {
          title: "Bloxite",
          year: "2022",
          description:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor",
          image: "/img/logo.png",
        },
      },
    };
  },
};
</script>

<style scoped lang="scss">
.line {
  width: 4px;
  height: 50%;
  background: #404040;
  position: absolute;
  border-radius: 8px;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}

.left-events {
  // make it at the exact left of the line with no space in between
  position: absolute;
  left: 0;
  top: 50%;
  transform: translateY(-50%);
  width: 100%;
  height: 100%;
  overflow: hidden;
  z-index: 1;
}

.right-events {
  // make it at the right side of the line
  position: absolute;
  top: 36%;
  right: 75%;
  transform: translate(-50%, -50%);
  width: 100%;
  height: 100%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  overflow: hidden;
}
</style>
