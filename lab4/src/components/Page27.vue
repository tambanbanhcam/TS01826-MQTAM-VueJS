<template lang="">
    <div>
        <h1>{{msg}}</h1>
        <h3 v-html="msg">HELOOOOOOO</h3>
        Count: {{ count }} <br>
        <button @click="increment">Tăng</button>
        <button @click="reset">Đặt lại</button>
        <button @click="count--">Giảm</button>
    </div>
</template>
<script>
export default {
data() {
return {
count: 0
};
},
methods: {
increment() {
this.count++;// Dùng this để truy cập biến trong data
},
reset() {
this.count = 0; //đặt lại count về 0
}
}
};
</script>
<style lang="">
    
</style>