<template>
  <div class="relative">
    <div class="h-12 w-5/6 flex items-center centered-bar absolute z-10">
      <div class="h-1/2 w-full bg-white rounded-md"></div>
    </div>
    <div
      class="h-12 w-5/6 flex items-center centered-bar absolute z-20"
      :class="`bar-container-${side}`"
      :style="style"
    >
      <div
        class="h-1/2 w-full rounded-md rainbow-bg"
        :class="`rainbow-bg-${side}`"
      ></div>
    </div>
  </div>
</template>

<script>
export default{
  props: {
    side: {
      default: 'left'
    },
    percentage: {
      default: 0
    }
  },
  computed: {
    style() {
      if (this.side === 'left') {
        const percentageTemp = this.percentage === 100 ? 110 : this.percentage;
        return {
          clipPath: `polygon(0 0, ${percentageTemp}% 0, ${percentageTemp}% 110%, 0 110%)`,
        }
      } else {
        return {
          clipPath: `polygon(${100 - this.percentage}% 0, 110% 0, 110% 110%, ${ 100 - this.percentage}% 110%)`,
        }
      }
    },
  },
}
</script>

<style scoped>
.bar-container-left {
  transition: clip-path 0.5s ease-in;
}

.rainbow-bg-left {
  background: linear-gradient(to right, red, orange, yellow, green, blue);
}

.bar-container-right {
  transition: clip-path 0.5s ease-in;
}

.rainbow-bg-right {
  background: linear-gradient(to left, red, orange, yellow, green, blue);
}

.rainbow-bg::after {
  content: '';
  position: absolute;
  z-index: inherit;
  top: 0px;
  bottom: 0px;
  left: 0px;
  right: 0px;
  margin: auto;
  height: 50%;
  width: 100%;
  opacity: 0.8;
  filter: blur(6px);
  background: inherit;
  border-radius: inherit;
}

.centered-bar {
  top: 0px;
  bottom: 0px;
  left: 0px;
  right: 0px;
  margin: auto;
}
</style>