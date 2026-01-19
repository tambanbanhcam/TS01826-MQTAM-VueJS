<template>
  <div>
    <button @click="isShowing = !isShowing" v-html="buttonContent"></button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isShowing: false 
    };
  },
  computed: {
    buttonContent() {
      return this.isShowing 
        ? '<b style="color: red;">HIDE</b>' 
        : '<i style="color: blue;">SHOW</i>';
    }
  }
};
</script>