# Reusable Components (Button)

It is quite possible, and encouraged to have a single component that can be used throughout the application.
This will have a few key benefits:

1. Enforce DRY methodology
2. Easier to debug

## How to build a reusable component

There are three main ways that VueJS components talk to each other
1. Vuex
2. Emitters
3. EventBus
4. Props

All are viable and all can/should be used together to achieve the desired results. 

The component that is being reused should not contain any logic besides resending what it was passed as a prop back up to the parent. 
A lot of times, you will have an array of these reusable components and they will do different things. For example, perhaps you want to add a menu and each button will proceed to log out different information. 

So you send the information that constructs the button (ie, the color, text and an id). Upon being clicked, send a identifier:

```
this.$emit('buttonClicked', id)
```

This id can then be used in the parent as an identifier to determine which button was clicked and what to do with it.

So in the template, receive the click:
```
<Button @buttonClicked="handleClick">
```

***** Note on the above that you don't need to specify the id in the tag, however it will be available to you in the method like so:


```
methods: {
  handleClick(id) {
    console.log(id)
  }
}
```
