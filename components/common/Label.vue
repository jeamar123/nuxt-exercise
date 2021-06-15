<template>
  <div 
    class="relative mb-2"
    :class="[containerClass]"
  >
    <component
      :is="element"
      :id="id"
      class="text-base"
      :class="[textClass]"
    >
      <slot/>
    </component>
  </div>
</template>

<script>
export default {
  name: 'Label',

  props: {
    id: {
      type: String,
    },
    element: {
      type: String,
      default: 'p',
    },
    containerClass: {
      type: String,
    },
    textClass: {
      type: String,
    },
  },
  computed: {
    
  },
};
</script>

<style lang="scss">


</style>
