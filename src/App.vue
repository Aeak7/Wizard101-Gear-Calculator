
<template>
  <div class="father">
  <div class="son">
    <div class="container" v-for="stat in stats">
      <div class="row">
        <div class="col">{{ stat }}</div>
      </div>
      <div class="row">
        <div class="col" v-for="school in schools"> <img :src="school.img"/> </div>
      </div>
      <div class="row">
        <div class="col" v-for="school in schools"></div>
      </div>
      <div class="row" v-if="stat === 'Damage' || stat === 'Resistance'">
        <div class="col" v-for="school in schools"></div>
      </div>
    </div>
  </div>
  <div class="son">
    <div class="container" v-for="gear in gear">
      <div class="row">
        <div class="gear">{{ gear }}</div>
      </div>
      <div class="row">
        <div class="gear"> <button type="button">Select Something</button> </div>
      </div>
    </div>
  </div>
</div>
</template>

<script>

export default {
  data() {
    return {
      gear: [
        'Hat', 'Robe', 'Boots', 'Wand', 'Athame', 'Amulet', 'Ring', 'Deck', 'Mount',
      ],
      stats: [
        'Damage', 'Resistance', 'Accuracy', 'Critical Rating', 'Block Rating', 'Pip Conservation',
      ],
      schools: [
        {name: 'fire', img: 'src/assets/img/fire.png'}, {name: 'ice', img: 'src/assets/img/ice.png'},
        {name: 'storm', img: 'src/assets/img/storm.png'}, {name: 'myth', img: 'src/assets/img/myth.png'},
        {name: 'life', img: 'src/assets/img/life.png'}, {name: 'death', img: 'src/assets/img/death.png'},
        {name: 'balance', img: 'src/assets/img/balance.png'}, {name: 'shadow', img: 'src/assets/img/shadow.png'},
      ]
    }
  }
}
</script>

