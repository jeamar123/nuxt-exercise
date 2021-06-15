<template>
  <div 
    class="relative h-8"
    :class="[
      containerClass,
      {
        'pr-6' : isSearch,
        'flex' : isJobSearch,
      }
    ]"
  >
    <label v-if="label != ''" :for="name" class="">
      {{ label }}
    </label>
    <component
      :is="element"
      :value.prop="value"
      :type="type"
      :id="name"
      :placeholder="placeholder"
      ref="inputRef"
      class="bg-transparent w-full h-full px-4"
      :class="[
        inputClass,
        {
          'rounded-30 mr-10' : isJobSearch
        }
      ]"

      @input="$emit('input', $event.target.value)"
      @blur="$emit('blur', $event)"
    />

    <img v-if="isSearch" src="~/assets/images/search-icon.png" alt="" class="w-4 absolute right-2.5 top-2">
    <img v-if="isJobSearch" src="~/assets/images/circle-arrow-blue.png" alt="" class="">

  </div>
</template>

<script>
export default {
  name: 'Input',

  props: {
    element: {
      type: String,
      default: 'input',
    },
    value: {
      type: String,
      default: '',
    },
    type: {
      type: String,
      default: 'text',
    },
    name: {
      type: String,
      required: true,
    },
    label: {
      type: String,
    },
    placeholder: {
      type: String,
    },
    isSearch: {
      type: Boolean,
    },
    isJobSearch: {
      type: Boolean,
    },
    containerClass: {
      type: String,
    },
    inputClass: {
      type: String,
    },
    placeholder: {
      type: String,
    },
  },
  computed: {
    
  },
};
</script>

<style lang="scss">


</style>
