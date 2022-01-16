<template>
	<nav class="fixed w-full flex justify-between items-center text-white bg-black z-50 shadow-md px-8">
    <div>
      Logo
    </div>
    <div class="flex">
      <a href="#" class="nav-item">About</a>
      <a href="#" class="nav-item">Traits</a>
      <a href="#" class="nav-item">RoadMap</a>
      <a href="#" class="nav-item">Sneak Peeks</a>
      <a href="#" class="nav-item">FAQ</a>
      <a href="#" class="nav-item">Team</a>
    </div>
    <div>
      <button class="px-3 py-1 border-2 border-white rounded-md">
        Contact
      </button>
    </div>
  </nav>
</template>

<style scoped>
.nav-item {
  @apply px-3;
  @apply py-8;
}

.nav-item:after {
  content: '';
  display: block;
  width: 100%;
  height: 5px;
  border-radius: 10px 10px 0 0;
  background-color: transparent;
  position: relative;
  @apply -bottom-8;
}

.nav-item:hover:after {
  background-color: white;
}
</style>