<template>
  <nav
    class="
      fixed
      w-full
	  grid
	  grid-cols-3
	  grid-rows-1
      items-center
      text-white
      bg-black
      z-50
      shadow-md
	  px-4
      md:px-8
	  h-16
	  md:h-20
	  box-border
    "
  >
    <div class="md:hidden px-2">
      <font-awesome-icon :icon="['fas', 'bars']" />
    </div>
    <div class="flex justify-center md:justify-start">Logo</div>
    <div class="hidden md:flex md:justify-center h-full">
      <a href="#" class="nav-item"><span>Home</span></a>
      <a href="#" class="nav-item"><span>Current Collection</span></a>
      <a href="#" class="nav-item"><span>Comin Soon</span></a>
    </div>
    <div class="flex justify-end">
      <button class="px-1.5 md:px-3 py-0.5 md:py-1 border-2 border-white rounded-md">
        Contact
      </button>
    </div>
  </nav>
</template>

<style scoped>
.nav-item {
  @apply px-3;
  @apply h-full;
  @apply flex;
  @apply items-center;
  position: relative;
}

.nav-item:after {
  content: '';
  display: block;
  width: calc(100% - (2 * 0.75rem));
  height: 5px;
  border-radius: 10px 10px 0 0;
  background-color: transparent;
  position: absolute;
  bottom: 0;
}

.nav-item:hover:after {
  background-color: white;
}
</style>