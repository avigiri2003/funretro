<template>
  <div class="negativeItems">
    <h2>Didn't work well</h2>
    <div>
      <input type="button" value="+" class="add-card">
    </div>
  </div>
</template>

<script>
export default {
  name: 'NegativeItems',
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.negativeItems{
  display: flex;
  min-width: 200px;
  padding-bottom: 15px;
  margin-left: 15px;
  flex-basis: 0;
  flex-direction: column;
  flex-grow: 1;
}

.negativeItems h2 {
  margin-top: 5px;
  margin-bottom: 5px;
  font-size: 1.2em;
  font-weight: normal;
}

.add-card{
  display: block;
  width: 100%;
  padding: 8px;
  margin: 0 0 10px;
  font-weight: bold;
  color: #555;
  background: #ddd;
  border: 0;
  font-size: 17px;
}

.add-card:hover{
  background: lightgrey;
  cursor: pointer;
}

</style>
