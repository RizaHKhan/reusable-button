<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png" />
    <Button v-for="(button, i) in buttons" :button="button" :key="i" @buttonClicked="handleClick"/>
  </div>
</template>

<script>
 import Button from '@/components/Button.vue'

export default {
  name: "Home",
  components: {
    Button
  },
  computed: {
    buttons() {
      let buttons = []

      const p1 = {
        id: 1, 
        conditionClass: 'danger',
        title: "Button 1",
        page: 'Home 1'
      }

      const p2 = {
        id: 2, 
        conditionClass: 'warning',
        title: "Button 2",
        page: 'Home 1'
      }
        
      const p3 = {
        id: 3, 
        conditionClass: 'success',
        title: "Button 3",
        page: 'Home 1'
      }

      buttons.push(p1)
      buttons.push(p2)
      buttons.push(p3)

      return buttons;
    }
  },
  methods: {
    handleClick(id) {
      console.log(id)
    }
  }
};
</script>
