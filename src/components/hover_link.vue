<script setup>
const props = defineProps({
  url: String,
  underline: {
    type: Boolean,
    default: false
  },
});
</script>

<template>
  <a :href="props.url" target='_blank' rel='noopener noreferrer' v-bind:class="props.underline === true ? 'underline' : ''">{{ text || url }}</a>
</template>

<style scoped>

a {
  text-decoration: none;
  display: inline-block;
  position: relative;
  color: var(--pre-color);
  height: fit-content;
  transition: all 0.25s ease-in-out;
  border-bottom: 2px solid transparent;
}

a:hover {
  color: var(--hover-color);
  border-bottom: 2px solid transparent;
}

a.underline:hover {
  border-bottom: 2px solid var(--hover-color);
}
</style>