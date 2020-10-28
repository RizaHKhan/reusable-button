<template>
  <div class="contact">
    <h1>This is the Contact Page</h1>
    <Button :button="button" @buttonClicked="handleClick"/>
  </div>
</template>

<script>
import Button from '@/components/Button'

export default { 
  components: { Button },
  data() {
    return {
      button: {
        conditionClass: 'danger',
        title: 'From Contact',
        page: 'Contact'
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
