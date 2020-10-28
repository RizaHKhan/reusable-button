<template>
  <button class="button" :class="{button.conditionClass}">
    {{ button.title }}
  </button>
</template>


<script>
export default {
  props: ['button']
}
</script>

<style>
  .button {
    border: solid 2px red;
    padding: 1rem 1.75rem;
  }
  .success {
    background: green;
  }

  .danger {
    background: red;
  }
</style>
