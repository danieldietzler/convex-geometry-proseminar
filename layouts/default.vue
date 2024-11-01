<template>
  <div class="slidev-layout layout flex flex-col">
    <slot />
  </div>
  <footer
    v-if="$slidev.nav.currentLayout !== 'cover'"
    class="absolute bottom-0 right-0 m-6 mr-10"
  >
    {{ $slidev.nav.currentPage }}/{{ $slidev.nav.total }}
  </footer>
</template>