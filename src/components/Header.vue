<template>
  <div class="header">
    <h3>This is Header</h3>
  </div>
</template>

<script>
export default {
  name: 'Header',
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.header{
  display: flex;
  flex-wrap: nowrap;
  background: #2196f3;
  width: 100%;
  min-height: 47px;
  box-sizing: border-box;
  padding-right: 15px;
  padding-left: 15px;
  color: white;
  justify-content: space-between;
  align-items: center;
  border-radius: 0;
}

</style>
