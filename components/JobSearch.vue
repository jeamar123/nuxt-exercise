<template>
  <Card 
    class="job-search-form bg-c-blue w-9/12 mx-auto h-64 text-center py-16 px-10"
  >
    <Label 
      containerClass="text-center mb-10"
      textClass="text-c-primary text-4xl font-bold"
    >
      Where do you need the job done?
    </Label>

    <Input
      v-for="(fieldProps, field) in form"
      :placeholder="fieldProps.placeholder"
      :isJobSearch="true"
      containerClass="h-16"
      inputClass="bg-white text-lg placeholder-c-primary"
      :key="field"
      v-model="fieldProps.value"
      :name="field"
      :label="fieldProps.label"
      :disabled="isLoading"
      :error="fieldProps.error"
      @blur="validateField(field, form)"
      @input="clearError(field, form)"
    />
  </Card>
</template>

<script>
import Input from '~/components/common/Input';
import Card from '~/components/common/Card';
import Label from '~/components/common/Label';
import { validateField, validateForm, clearError } from '~/helpers/validation';

export default {
  name: 'JobSearch',
  props: {
    
  },
  components: {
    Input,
    Card,
    Label
  },
  data: () => ({
    hasError: false,
    isLoading: false,
    errorMsg: '',
    form: {
      search: {
        value: '',
        error: '',
        rules: [],
        placeholder: 'Manchester',
        label: '',
      },
    },
  }),
  computed: {},
  methods: {
    validateField,
    validateForm,
    clearError,
    clearErrors() {
      if (this.hasError) this.hasError = false;
      if (this.errorMsg) this.errorMsg = '';
    },
  },
};
</script>

<style lang="scss">
  .job-search-form{
    border-radius: 50px;
  }
</style>