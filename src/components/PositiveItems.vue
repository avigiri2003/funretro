<template>
  <div class="positiveItems">
    <h2>Went well</h2>
    <div>
      <input type="button" value="+" class="add-card" @click="newCard">
    </div>
    <div>
      <PositiveCards :cards="cards" @addCard="addCard($event)"/>
    </div>
  </div>
</template>

<script>
import PositiveCards from './PositiveCards.vue'

export default {
  name: 'PositiveItems',
  components: {
    PositiveCards
  },
  data(){
    return {
      cards:[
        {
        description: 'test 123',
        created: '',
        added: true
        },
        {
        description: 'test 4292',
        created: '',
        added: true
        }
      ]
    }
  },
  methods: {
    newCard() {
      this.cards.push({description: '', created: '', added: false});
    },
    addCard(data){
      console.log(data.index, data.description);
      this.cards[data.index].description = data.description;
      this.cards[data.index].created = '';
      this.cards[data.index].added = true;
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.positiveItems{
  display: flex;
  min-width: 200px;
  padding-bottom: 15px;
  margin-left: 15px;
  flex-basis: 0;
  flex-direction: column;
  flex-grow: 1;
}

.positiveItems h2 {
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
