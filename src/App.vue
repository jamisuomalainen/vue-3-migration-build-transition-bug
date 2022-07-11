<template>
  <div id="app">
    <button type="button" @click="showText = !showText">
      Toggle text
    </button>

    <Transition
      enter-active-class="transition-duration"
      enter-from-class="opacity-0"
      enter-to-class="opacity-100"
      leave-active-class="transition-duration"
      leave-from-class="opacity-100"
      leave-to-class="opacity-0"
    >
      <p v-if="showText">
        The quick brown fox jumps over the lazy dog
      </p>
    </Transition>
  </div>
</template>

<script>
export default {
  data: () => ({
    showText: true
  })
}
</script>

<style>
.transition-duration {
  transition-duration: 500ms;
}

.opacity-0 {
  opacity: 0;
}

.opacity-100 {
  opacity: 100;
}
</style>
