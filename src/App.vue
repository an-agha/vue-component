<template>
    <h1> {{title}}</h1>
    <input type="text" placeholder="Product" ref="name">
    <button @click="handleClick">Click Me</button>
    <div class="product-container">
        <product v-for="zzzzzzzzzzz in arr" :key="product.id"/>
    </div>

</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'

// import components
import product from './components/product.vue'
export default {
  name: 'App',
  components: {product},
   data() {
      return {
        title: 'My First Vue App',
        arr : [
          {
            id: 1,
            name: 'Shirt',
            rate: 1200
          },
          {
            id: 2,
            name: 'T Shirt',
            rate: 1200
          },
          {
            id: 3,
            name: 'Skirt',
            rate: 1200
          }
        ]
      }
   },
   methods: {
    handleClick() {
      // console.log(this.$refs.name);
      this.$refs.name.classList.add('input')
      this.$refs.name.focus()
    }
   }
  }
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.product-container {
  width:100%;
  display:flex;
  align-items: center;
  justify-content:center;
  flex-wrap:wrap;
  column-gap:20px;
  row-gap:20px;
  margin:2vh 0
}
.input {
  background: #ece;
}
</style>
