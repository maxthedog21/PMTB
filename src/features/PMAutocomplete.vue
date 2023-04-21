<template>
  <div class="pt-0 pb-2">
    <label class="label-button"> {{ label }} </label>
    <v-autocomplete
      @input="onChange"
      v-model="items[0]"
      :items="items"
      :value="value"
      density="compact"
      variant="outlined"
      hide-details=""
      color="#1976d2"
      class="field"
      :style="newStyle"
    ></v-autocomplete>
  </div>
</template>
<script>
export default {
  name: "CBSAutocomplete",
  props: {
    item: {
      required: true,
    },
    items: {
      required: true,
    },
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
.page-padding {
  padding: 1.7em 1.8em 3.5em 1.8em;
}
.label-button {
  font-weight: 700 !important;
  color: #112e51 !important;
}
.field {
  padding-top: 3px !important;
}
.v-field__input input {
  box-shadow: none !important;
}
</style>
