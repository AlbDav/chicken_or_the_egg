<template>
  <div class="h-full w-full mx-auto flex flex-col justify-around">
    <kinesis-element :strength="5">
      <div class="h-5 w-5/6 bg-white mx-auto rounded-md">
      <div class="h-full w-full rainbow-bg rounded-md relative" :class="`rainbow-bg-${side}`">
      </div>
      </div>
    </kinesis-element>
    <kinesis-element
      class="h-1/2 w-5/6 rounded-md bg-white mx-auto"
      :strength="2"
    >
      Verso giusto
    </kinesis-element>
    <div class="w-5/6 h-1/6 mx-auto flex flex-col justify-end">
      <button
        class="w-full py-3 bg-custom-green rounded-md button-shadow"
        @click="vote"
      >
        Vota
      </button>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    side: {
      default: 'left'
    }
  },
  methods: {
    vote() {
      console.log('vote')
    },
  },
  mounted() {
    console.log(this.side);
  }
}
</script>

<style scoped>
.rainbow-bg-left {
  background: linear-gradient(to right, red, orange, yellow, green, blue);
}

.rainbow-bg-right {
  background: linear-gradient(to left, red, orange, yellow, green, blue);
}

.rainbow-bg::after {
  content: "";
  position: absolute;
  z-index: -1;
  bottom: 0px;
  left: 0px;
  height: 115%;
  width: 100%;
  opacity: 0.8;
  filter: blur(6px);
  background: inherit;
  border-radius: inherit;
}
</style>