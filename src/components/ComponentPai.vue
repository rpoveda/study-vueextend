<template>
    <div v-html="components" />
</template>

<script>
import ComponentFilho from './ComponentFilho.vue';
import Vue from 'vue';
export default {
  data() {
    return {
      components: ''
    }
  },
  mounted() {
    for (let index = 0; index < 5; index++) {
      const _class = Vue.extend(ComponentFilho);
      const _component = new _class({
        propsData: {
          texto: `Ola mundo ${index};`,
          showImage: true
        }
      })
      _component.$mount()
      this.components += _component.$el.innerHTML + "<br />"
      _component.$destroy()
    }
    console.log('components', this.components)
  }
}
</script>

<style>
</style>
