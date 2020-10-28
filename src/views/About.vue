<template>
  <div class="about">
    <h1>This is an about page</h1>
    <Button :button="button">
  </div>
</template>

<script>
import Button from '@/components/Button'

export default { 
  components: { Button },
  data() {
    return {
      button: {
        class: 'success',
        title: 'From About'
      }
    }
  }

}
</script>
