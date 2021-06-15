<template>
  <div id="main-content" class="mx-auto">
    <JobSearch/>
    
  </div>
</template>

<script>
import JobSearch from '~/components/JobSearch';
export default {
  name: 'Home',
  components: {
   JobSearch
  },
}
</script>

<style lang="scss">
  #main-content{
    max-width: 1016px;
  }
</style>
