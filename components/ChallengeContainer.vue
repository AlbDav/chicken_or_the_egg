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
        <kinesis-element :strengh="7">
          <img src="../static/Street_Fighter_VS_logo.png" alt="VS" />
        </kinesis-element>
      </div>
      <div
        class="h-full w-full grid grid-cols-2 gap-4 justify-center items-center"
      >
        <ChallengeItem side="left" />
        <ChallengeItem side="right" />
      </div>
    </div>
  </kinesis-container>
</template>