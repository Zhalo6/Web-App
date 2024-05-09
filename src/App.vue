<script setup>
import { ref } from 'vue'

const text = ref('')
const page = ref(0)
//const 1CostChampList = ref([Ahri, Caitlyn, Cho'Gath, Darius, Garen, Jax, Kha'Zix, Kobuko, Kog'maw, Malphite, Rek'Sai, Sivir, Yasuo])
//const 2CostChampList = ref([Aatrox, Gnar, Janna, Kindred, Lux, Neeko, Qiyana, Riven, Senna, Shen, Temmo, Yorick, Zyra])
//const 3CostChampList = ref([Alune, Amumu, Aphelios, Diana, illaoi, Soraka, Tahm Kench, Thresh, tristana, Volibear, Yone, Zoe])
//const 4CostChampList = ref([Annie, Ashe, Galio, Kai'Sa, Kayn, Lee Sin, Lillia, Morgana, Nautilus, Ornn, Sylas, Syndra])
//const 5CostChampList = ref([Azir, Hwei, Irelia, Lissandra, Sett, Udyr, Wukong, Xayah/Rakan])
//const componentList = ref([Sword, Bow, Rod, Tear, Chain Vest, Negatron Cloak, Giants Belt, Sparring Gloves])
//const itemList = ref[(Deathblade, Giant Slayer, Hextech Gunblade, Spear of Shojin, Edge of Night, Bloodthirster, Sterak's, Infinity Edge, Red Buff, Guinsoo's Rageblade, Static Shiv, Titan's Resolve, Runaan's Hurricane, Nashor's, Tooth, Last Whisper, Rabadon's Deathcap, Archangel's Staff, CrownGuard, Ionic Spark, Morellonomicon, Jeweled Gauntlet, Blue Buff, Protector's Vow, Adaptive Helm, Redemption, Hand of Justice, Bramble Vest, Gargoyle Stoneplate, Sunfire Cape, Steadfast Heart, Dragon's Claw, Evenshroud, Quicksilver, Warmog's Armour, Guardbreaker, Theif's Gloves)]

function onInput(e) {
  text.value = e.target.value
}

function reset() {
  page.value = 0
}
  
function teamComp() {
  page.value = 1
}

function bestInSlot() {
  page.value = 2
}

function augments() {
  page.value = 3
}
</script>

<style>
  .background {
    position: absolute;
    top: 0%;
    left: 0%;
    width: 1920px;
    height: 1080px;
    background: #102531;
  }   
  .backgroundTC {
    position: absolute;
    top: 0%;
    left: 0%;
    width: 1920px;
    height: 1080px;
    background: #102531;
  }
  .backgroundBIS {
    position: absolute;
    top: 0%;
    left: 0%;
    width: 1920px;
    height: 1080px;
    background: #102531;
  }
  .backgroundAUG {
    position: absolute;
    top: 0%;
    left: 0%;
    width: 1920px;
    height: 1080px;
    background: #102531;
  }
  .center {
    position: absolute;
    top: 150%;
    left: 50%;
    transform: translate(-50%, -50%);
    padding: 10px;
    background: #09202D;
    box-shadow: 0px 4px 8px 3px rgba(0, 0, 0, 0.15), 0px 1px 3px rgba(0, 0, 0, 0.3);
    border-radius: 4px;
  }
  .buttonZero {
    position: absolute;
    top: 50%;
    left: 7%;
    transform: translate(-50%, -50%);
    padding: 10px;
    background: #09202D;
    box-shadow: 0px 7px 21px rgba(0, 0, 0, 0.2);
    border-radius: 6px;
  }
  .buttonOne {
    position: absolute;
    top: 250%;
    left: 25%;
    transform: translate(-50%, -50%);
    padding: 10px;
    background: #09202D;
    box-shadow: 0px 7px 21px rgba(0, 0, 0, 0.2);
    border-radius: 6px;
  }
  .buttonTwo {
    position: absolute;
    top: 250%;
    left: 50%;
    transform: translate(-50%, -50%);
    padding: 10px;
    background: #09202D;
    box-shadow: 0px 7px 21px rgba(0, 0, 0, 0.2);
    border-radius: 6px;
  }
  .buttonThree {
    position: absolute;
    top: 250%;
    left: 75%;
    transform: translate(-50%, -50%);
    padding: 10px;
    background: #09202D;
    box-shadow: 0px 7px 21px rgba(0, 0, 0, 0.2);
    border-radius: 6px;
  }
  .titleStyle {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    padding: 4px 8px;
    gap: 10px;

    position: absolute;
    width: 228px;
    height: 46px;
    min-height: 24px;
    left: 65px;
    top: -20px;

    background: #09202D;
    box-shadow: 0px 4px 4px rgba(0, 0, 0, 0.25), 0px 4px 4px rgba(0, 0, 0, 0.25);
    color: #FFFFFF;
  }
  .listOneStyle {
    box-sizing: border-box;

    position: absolute;
    width: 300px;
    height: 300px;
    left: -5px;
    top: 50px;

    background: #09202D;
    border: 1px solid #09202D;
    color: #FFFFFF;
  }
  .listTwoStyle {
    box-sizing: border-box;

    position: absolute;
    width: 200px;
    height: 370px;
    left: 320px;
    top: -20px;

    background: #09202D;
    border: 1px solid #09202D;
    color: #FFFFFF;
  }
  .listThreeStyle {
    box-sizing: border-box;

    position: absolute;
    width: 200px;
    height: 370px;
    left: 545px;
    top: -20px;

    background: #09202D;
    border: 1px solid #09202D;
    color: #FFFFFF;
  }
  .imageStyle {
    position: absolute;
    width: 450px;
    height: 390px;
    left: 300px;
    top: -20px;
  }
</style>

<template>
  <div class="background"></div>
  <div class="center">
    <input :value="text" @input="onInput" placeholder="Enter Champion...">
  </div>
  <div class="buttonOne">
    <button @click="teamComp">Team Comps</button>
  </div>
  <div class="buttonTwo">
    <button @click="bestInSlot">Best in Slot</button>
  </div>
  <div class="buttonThree">
    <button @click="augments">Augments</button>
  </div>
  <div v-if="page == 1">
    <div class="backgroundTC"></div>
    <h1 class="titleStyle">Team Comps</h1>
    <h2 class="listOneStyle">Champion...</h2>
    <h2 class="listTwoStyle">Champion Info...</h2>
    <h2 class="listThreeStyle">Champion Comps...</h2>
  </div>
  <div v-if="page == 2">
    <div class="backgroundBIS"></div>
    <h1 class="titleStyle"> Best in Slot </h1>
    <h2 class="listOneStyle">Item...</h2>
    <h2 class="listTwoStyle">Item Info...</h2>
    <h2 class="listThreeStyle">Item Recipe...</h2>
  </div>
  <div v-if="page == 3">
    <div class="backgroundAUG"></div>
    <h1 class="titleStyle"> Augments </h1>
    <img class="imageStyle" src="/augmentChart.PNG">
  </div>
  <div class="buttonZero">
  <button @click="reset">Reset</button>
  </div>
</template>