<template>
  <button class="fancy-button" @click="handleClick">
    {{ buttonText }}
    <slot />
  </button>
</template>

<script>
export default {
  props: {
    buttonText: {
      type: String,
      required: true
    }
  },
  methods: {
    handleClick() {
      this.$emit('customClick')
    }
  }
}
</script>
