<template>
  <div>
    <pre>
      {{ button }}
    </pre>
    <button class="button" :class='button.conditionClass' @click="handleClick">
      {{ button.title }}
    </button>
  </div>
</template>


<script>
export default {
  props: {
    button: {
      type: Object,
      required: true
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
