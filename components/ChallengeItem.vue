<template>
  <div class="h-full w-full mx-auto flex flex-col justify-around">
    <kinesis-element :strength="5">
      <LifeBar :percentage="percentage" :side="side" />
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
      default: 'left',
    },
  },
  data() {
    return {
      percentage: 0,
    }
  },
  methods: {
    vote() {
      console.log('vote')
    },
  },
  mounted() {
    setTimeout(() => {
      this.percentage = Math.floor(Math.random() * 100) + 1;
    }, 1000)
  },
}
</script>