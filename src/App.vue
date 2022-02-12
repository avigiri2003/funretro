<template>
  <div id="app">
    <div>
      <Header />
    </div>
    <div class="container">
      <PositiveItems />
      <NegativeItems />
      <ActionItems />
    </div>
  </div>
</template>

<script>
import Header from './components/Header.vue'
import PositiveItems from './components/PositiveItems.vue'
import NegativeItems from './components/NegativeItems.vue'
import ActionItems from './components/ActionItems.vue'

export default {
  name: 'App',
  components: {
    Header,
    PositiveItems,
    NegativeItems,
    ActionItems
  }
}
</script>

<style>
body {
  font-family: "Franklin Gothic Medium", "Arial Narrow", Arial, sans-serif;
  line-height: 1.6;
  background: #e8f7f0;
  margin: 0px;
}
.container {
  display: flex;
  width: 100%;
  min-height: calc(100vh - 100px);
  padding-bottom: 35px;
  overflow-x: auto;
  background: #f3f3f3;
  
}
</style>
