<template>
  <kinesis-container class="h-full w-full">
    <div class="h-full w-full">
      <div class="w-full text-center text-white">Here, you can put</div>
      <div class="h-full w-full grid grid-cols-2 gap-4 justify-center items-center">
        <kinesis-element class="h-5/6 w-5/6 rounded-md bg-white mx-auto" :strength="50">
          Verso giusto
        </kinesis-element>
        <kinesis-element class="h-5/6 w-5/6 rounded-md bg-white mx-auto" :strength="50">
          Verso sbagliato
        </kinesis-element>
      </div>
    </div>
  </kinesis-container>
</template>

<script>
export default {
  name: 'IndexPage',
}
</script>
