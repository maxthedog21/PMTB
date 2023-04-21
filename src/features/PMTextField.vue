<template>
  <div class="pt-0 pb-2">
    <label class="label-button"> {{ label }}</label>
    <v-text-field
      @input="onChange"
      :value="value"
      :placeholder="placeholder"
      hide-details
      density="compact"
      variant="outlined"
      color="#1976d2"
      class="field"
      :style="newStyle"
    ></v-text-field>
  </div>
</template>
<script>
export default {
  name: "CBSTextField",
  props: {
    value: {
      required: true,
    },
    placeholder: {
      required: true,
    },
    label: {
      required: true,
    },
    newStyle: {
      default: "",
      required: false,
    },
  },
  methods: {
    onChange(newValue) {
      this.$emit("onChange", newValue);
    },
  },
};
</script>
<style lang="scss">
@import "../colors.module";
.label-button {
  font-weight: 700 !important;
  color: #112e51 !important;
}
.field {
  padding-top: 3px !important;
  input {
    box-shadow: none !important;
  }
}
</style>
