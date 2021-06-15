<template>
  <div 
    class="rounded-md p-5"
    :class="[containerClass]"
  >
    <slot/>
  </div>
</template>

<script>
export default {
  name: 'Card',
  props: {
    containerClass: {
      type: String,
    },
  },
  computed: {
    
  },
};
</script>

<style lang="scss">


</style>
