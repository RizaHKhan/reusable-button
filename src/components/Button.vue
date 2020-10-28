<template>
  <button class="button" :class='button.conditionClass' @click="handleClick">
    {{ button.title }}
  </button>
</template>


<script>
export default {
  props: {
    button: {
      type: Object,
      required: true,
    }
  },
  methods: {
    handleClick() {
      const id = this.button.id ? this.button.id : false
      this.$emit('buttonClicked', id)
    }
  }
}
</script>

<style>
  .button {
    border: solid 2px black;
    padding: 1rem 1.75rem;
    margin: 0.5em;
  }
  .success {
    background: green;
  }

  .danger {
    background: red;
  }

  .warning { 
    background: yellow;
  }

</style>
