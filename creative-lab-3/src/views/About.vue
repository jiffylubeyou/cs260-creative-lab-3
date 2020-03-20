<template>
  <div class="about">
    <h1>Hello. This page is where you will be constructing your sandwich.</h1>
    <div class="paragraph">
    <p>There are lots of options to chose from, so just click whatever and add it to your sandwich. It's not very hard so if you still have trouble then you're probably beyond saving.</p>
    </div>
    <div>
    <ProductList :products="products"/>
    </div>
  </div>
</template>

<style>
.paragraph {
  color: brown;
  text-align: center;
  padding: 100px ;
}

<script>
import HelloWorld from "../components/HelloWorld.vue"
export default {
  name: 'Home',
  components: {
    HelloWorld
  },
  data() {
    return {
    }
  },
  computed: {
    products() {
      return this.$root.$data.products;
    }
  },
}
</script>
</script>
