<template>
  <fieldset id="fieldset">
    <legend>{{ label }}</legend>
    <div>
      <component :is="isInput ? 'input' : 'select'" :placeholder="placeholder" :type="type">
        <option
          v-if="!isInput"
          v-for="option in options"
          :key="option.value"
          :value="option.value"
        >
          {{ option.label }}
        </option>
      </component>
    </div>
  </fieldset>
</template>

<script>
export default {
  name: "Fieldset",
  props: {
    isInput: {
      type: Boolean,
      default: true,
    },
    placeholder: {
      type: String,
      default: "",
    },
    label: {
      type: String,
      default: "Fieldset Label",
    },
    type: {
      type: String,
      default: "text",
    },
    options: {
      type: Array,
      default: () => [],
    },
  },
};
</script>

<style>
#fieldset {
  width: 100%;
  margin: 15px 0;
  border: 1px solid #f5f5f5;
  padding: 10px 5px;
  border-radius: 8px;
}

#fieldset legend {
  padding: 0 5px;
}

#fieldset input {
  width: 100%;
}

</style>
