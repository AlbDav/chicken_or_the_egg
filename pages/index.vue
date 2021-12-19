<template>
  <kinesis-container class="h-full w-full">
    <div class="h-full w-full">
      <div
        class="
          h-full
          w-full
          text-center text-white
          z-10
          absolute
          flex
          justify-center
          items-center
		  pointer-events-none
        "
      >
        <kinesis-element :strengh="10">
          <img src="../static/Street_Fighter_VS_logo.png" alt="VS" />
        </kinesis-element>
      </div>
      <div
        class="h-full w-full grid grid-cols-2 gap-4 justify-center items-center"
      >
        <div class="h-full w-full mx-auto flex flex-col justify-around">
          <kinesis-element
            class="h-1/2 w-5/6 rounded-md bg-white mx-auto"
            :strength="15"
          >
            Verso giusto
          </kinesis-element>
          <div class="w-5/6 h-1/6 mx-auto flex flex-col justify-end">
            <button
              class="
                w-full
                py-3
                bg-custom-green
                rounded-md
                border-b-8
                active:border-b
                border-custom-dark-green
              "
              @click="vote"
            >
              Vota
            </button>
          </div>
        </div>
        <kinesis-element
          class="h-5/6 w-5/6 rounded-md bg-white mx-auto"
          :strength="15"
        >
          Verso sbagliato
        </kinesis-element>
      </div>
    </div>
  </kinesis-container>
</template>

<script>
export default {
  name: 'IndexPage',
  methods: {
    vote() {
      console.log('vote')
    },
  },
}
</script>
