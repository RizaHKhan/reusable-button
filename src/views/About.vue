<template>
  <div class="about">
    <h1>This is an about page</h1>
    <Button :button="button" @buttonClicked="handleClick" />
  </div>
</template>

<script>
import Button from '@/components/Button'

export default { 
  components: { Button },
  data() {
    return {
      button: {
        conditionClass: 'success',
        title: 'From About',
        page: 'About',
      }
    }
  },
  methods: {
    handleClick() {
      console.log(`Clicked from ${this.button.page}`)
    }
  }

}
</script>
