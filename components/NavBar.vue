<template>
	<nav class="fixed w-full flex justify-between items-center text-white bg-black z-50">
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

.nav-item:hover:after {
  content: '';
  display: block;
  width: 100%;
  height: 5px;
  border-radius: 10px 10px 0 0;
  background-color: white;
  position: relative;
  bottom: -2rem;
  z-index: 100;
}
</style>