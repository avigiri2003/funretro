<template>
  <div class="positiveCards">
    <div v-for="(card, index) in cards" :key="index" >
      <!-- {{ card.description }} -->
      <!-- <input type="text" v-model="card.description"> -->
      <textarea 
        v-model="card.description" 
        :class="[card.added ? 'card-added' : '']"
        :disabled="card.added" />
      <button 
        class="add-card" 
        @click="$emit('addCard', {index:index, description:card.description})"
        :class="[card.added ? 'hide-add-button' : '']"
        :disabled="card.description === ''"
      >ADD</button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'PositiveCards',
  props:{
    cards: Array,
    // addCard: Function
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.positiveCards div{
  display: flex;
  position: relative;
  min-width: 200px;
  padding-bottom: 10px;
  /* margin-left: 15px; */
  flex-basis: 0;
  flex-direction: column;
  flex-grow: 1;
}

.positiveCards textarea{
  position: relative;
  border: 4px solid #009688;
  overflow: hidden;
  overflow-wrap: break-word;
  resize: none;
  /* width: 100%; */
  height: 55px;
  font-family: -apple-system,BlinkMacSystemFont,'Roboto',sans-serif;
  font-size: 15px;
}

.add-card{
  position: absolute;
  bottom: 20px;
  left: 10px;
  width: 43px;
  height: 20px;
  padding: 0;
  margin-left: 0;
  font-size: .7em;
  /* line-height: 2em; */
  color: white;
  background: #00c853;
  border-bottom: 2px solid #00a946;
  cursor: pointer;
  
}

.add-card:disabled{
  cursor: not-allowed;
}
.hide-add-button{
  display: none;
}

.card-added{
  background: #009688;
  color:white;
}

/*.add-card:hover{
  background: lightgrey;
  cursor: pointer;
} */

</style>
