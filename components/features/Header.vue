<template>
  <div class="flex md:py-12 md:px-16 py-5 px-8">
    <div class="flex-1 flex items-center">
      <label for="" class="text-c-primary ff-product-sans-bold text-2xl">localpro</label>
      <img src="~/assets/images/header-arrow.png" alt="" class="w-4 h-6 ml-2">
    </div>
    <div class="flex items-center justify-end">
      <div class="w-7 mx-2.5">
        <div class="rounded-full w-7 h-7 bg-c-yellow flex items-center justify-center font-bold text-white">
          S
        </div>
      </div>
      <div class="mx-2.5">
        <label for="" class="font-bold text-xl text-c-primary">Samantha</label>
      </div>
      <div class="ml-8">
        <Input
          v-model="searchVal"
          type="text"
          name="header-search"
          label=""
          :isSearch="true"
          containerClass="bg-gray-200 rounded-2xl w-48 h-8"
          inputClass=""
        />
      </div>
    </div>
  </div>
</template>

<script>
import Input from '~/components/common/Input';
// import UserMenu from '~/components/nav/UserMenu';

export default {
  name: 'Header',
  props: {},
  components: {
    Input,
    // UserMenu,
  },
  data: () => ({
    searchVal: ''
  }),
  computed: {
    
  },
  methods: {
    
  },
};
</script>

<style lang="scss">
</style>
