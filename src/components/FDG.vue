<script setup lang="ts">
import {ref, computed} from "vue";

const defaultRateOfFire = ref(0);

const defaultReload = ref(0);
const equipmentReload = ref(0);
const fleetTechnology = ref(0);
const meowfficer = ref(0);

const skill1 = ref(0);
const skill2 = ref(0);
const skill3 = ref(0);

const sonataOfChaos = ref(50);

const highPeformanceFireControllRader = ref(false);
const experimentalGunBarrel = ref(false);

const firstAttack = computed(
  (): number => {
    let attackTime =  defaultRateOfFire.value * Math.sqrt( 200 / ( 100 + ( defaultReload.value + equipmentReload.value + fleetTechnology.value + meowfficer.value ) * (1 + skill1.value/100 + skill2.value/100 + skill3.value/100 )));
    if(highPeformanceFireControllRader.value){
      attackTime = attackTime * 0.85;
    }
    attackTime = (Math.floor(attackTime * 100)) / 100;
    return attackTime;
  }
)
const secondAttack = computed(
  (): number => {
    let attackTime =  defaultRateOfFire.value * Math.sqrt( 200 / ( 100 + ( defaultReload.value + equipmentReload.value + fleetTechnology.value + meowfficer.value ) * (1 + skill1.value/100 + skill2.value/100 + skill3.value/100 + sonataOfChaos.value/100)));
    attackTime = (Math.floor(attackTime * 100)) / 100;
    return attackTime;
  }
)
const thirdAttack = computed(
  (): number => {
    let attackTime =  defaultRateOfFire.value * Math.sqrt( 200 / ( 100 + ( defaultReload.value + equipmentReload.value + fleetTechnology.value +meowfficer.value ) * (1 + skill1.value/100 + skill2.value/100 + skill3.value/100)));
    attackTime = (Math.floor(attackTime * 100)) / 100;
    return attackTime;
  }
)
const fourthAttack = computed(
  (): number => {
    let attackTime =  defaultRateOfFire.value * Math.sqrt( 200 / ( 100 + ( defaultReload.value + equipmentReload.value + fleetTechnology.value + meowfficer.value ) * (1 + skill1.value/100 + skill2.value/100 + skill3.value/100 + sonataOfChaos.value/100 )));
    attackTime = (Math.floor(attackTime * 100)) / 100;
    return attackTime;
  }
)
const fifthAttack = computed(
  (): number => {
    let attackTime =  defaultRateOfFire.value * Math.sqrt( 200 / ( 100 + ( defaultReload.value + equipmentReload.value + fleetTechnology.value + meowfficer.value ) * (1 + skill1.value/100 + skill2.value/100 + skill3.value/100 )));
    if(experimentalGunBarrel.value) {
      attackTime = attackTime * 1.35;
    }
    attackTime = (Math.floor(attackTime * 100)) / 100;
    return attackTime;
  }
)
const sixthAttack = computed(
  (): number => {
    let attackTime =  defaultRateOfFire.value * Math.sqrt( 200 / ( 100 + ( defaultReload.value + equipmentReload.value + fleetTechnology.value + meowfficer.value ) * (1 + skill1.value/100 + skill2.value/100 + skill3.value/100 +sonataOfChaos.value/100 )));
    if(experimentalGunBarrel.value) {
      attackTime = attackTime * 1.35;
    }
    attackTime = (Math.floor(attackTime * 100)) / 100;
    return attackTime;
  }
)
const seventhAttack = computed(
  (): number => {
    let attackTime =  defaultRateOfFire.value * Math.sqrt( 200 / ( 100 + ( defaultReload.value + equipmentReload.value + fleetTechnology.value + meowfficer.value ) * (1 + skill1.value/100 + skill2.value/100 + skill3.value/100 )));
    if(experimentalGunBarrel.value) {
      attackTime = attackTime * 1.35;
    }
    attackTime = (Math.floor(attackTime * 100)) / 100;
    return attackTime;
  }
)
const eighthAttack = computed(
  (): number => {
    let attackTime =  defaultRateOfFire.value * Math.sqrt( 200 / ( 100 + ( defaultReload.value + equipmentReload.value + fleetTechnology.value + meowfficer.value ) * (1 + skill1.value/100 + skill2.value/100 + skill3.value/100 +sonataOfChaos.value/100 )));
    if(experimentalGunBarrel.value) {
      attackTime = attackTime * 1.35;
    }
    attackTime = (Math.floor(attackTime * 100)) / 100;
    return attackTime;
  }
)
const ninthAttack = computed(
  (): number => {
    let attackTime =  defaultRateOfFire.value * Math.sqrt( 200 / ( 100 + ( defaultReload.value + equipmentReload.value + fleetTechnology.value + meowfficer.value ) * (1 + skill1.value/100 + skill2.value/100 + skill3.value/100 )));
    if(experimentalGunBarrel.value) {
      attackTime = attackTime * 1.35;
    }
    attackTime = (Math.floor(attackTime * 100)) / 100;
    return attackTime;
  }
)
const tenthAttack = computed(
  (): number => {
    let attackTime =  defaultRateOfFire.value * Math.sqrt( 200 / ( 100 + ( defaultReload.value + equipmentReload.value + fleetTechnology.value + meowfficer.value ) * (1 + skill1.value/100 + skill2.value/100 + skill3.value/100 +sonataOfChaos.value/100 )));
    if(experimentalGunBarrel.value) {
      attackTime = attackTime * 1.35;
    }
    attackTime = (Math.floor(attackTime * 100)) / 100;
    return attackTime;
  }
)
const eleventhAttack = computed(
  (): number => {
    let attackTime =  defaultRateOfFire.value * Math.sqrt( 200 / ( 100 + ( defaultReload.value + equipmentReload.value + fleetTechnology.value + meowfficer.value ) * (1 + skill1.value/100 + skill2.value/100 + skill3.value/100 )));
    if(experimentalGunBarrel.value) {
      attackTime = attackTime * 1.35;
    }
    attackTime = (Math.floor(attackTime * 100)) / 100;
    return attackTime;
  }
)
const twelfthAttack = computed(
  (): number => {
    let attackTime =  defaultRateOfFire.value * Math.sqrt( 200 / ( 100 + ( defaultReload.value + equipmentReload.value + fleetTechnology.value + meowfficer.value ) * (1 + skill1.value/100 + skill2.value/100 + skill3.value/100 +sonataOfChaos.value/100 )));
    if(experimentalGunBarrel.value) {
      attackTime = attackTime * 1.35;
    }
    attackTime = (Math.floor(attackTime * 100)) / 100;
    return attackTime;
  }
)

const cumulativeSecondAttack = computed(
  (): number => {
    let attackTime = firstAttack.value + secondAttack.value;
    attackTime = (Math.floor(attackTime * 100)) / 100;
    return attackTime;
  }
)
const cumulativeThirdAttack = computed(
  (): number => {
    let attackTime = firstAttack.value + secondAttack.value + thirdAttack.value;
    attackTime = (Math.floor(attackTime * 100)) / 100;
    return attackTime;
  }
)
const cumulativeFourthAttack = computed(
  (): number => {
    let attackTime = firstAttack.value + secondAttack.value + thirdAttack.value + fourthAttack.value;
    attackTime = (Math.floor(attackTime * 100)) / 100;
    return attackTime;
  }
)
const cumulativeFifthAttack = computed(
  (): number => {
    let attackTime = firstAttack.value + secondAttack.value + thirdAttack.value + fourthAttack.value + fifthAttack.value;
    attackTime = (Math.floor(attackTime * 100)) / 100;
    return attackTime;
  }
)
const cumulativeSixthAttack = computed(
  (): number => {
    let attackTime = firstAttack.value + secondAttack.value + thirdAttack.value + fourthAttack.value + fifthAttack.value + sixthAttack.value;
    attackTime = (Math.floor(attackTime * 100)) / 100;
    return attackTime;
  }
)
const cumulativeSeventhAttack = computed(
  (): number => {
    let attackTime = firstAttack.value + secondAttack.value + thirdAttack.value + fourthAttack.value + fifthAttack.value + sixthAttack.value + seventhAttack.value;
    attackTime = (Math.floor(attackTime * 100)) / 100;
    return attackTime;
  }
)
const cumulativeEighthAttack = computed(
  (): number => {
    let attackTime = firstAttack.value + secondAttack.value + thirdAttack.value + fourthAttack.value + fifthAttack.value + sixthAttack.value + seventhAttack.value + eighthAttack.value;
    attackTime = (Math.floor(attackTime * 100)) / 100;
    return attackTime;
  }
)
const cumulativeNinthAttack = computed(
  (): number => {
    let attackTime = firstAttack.value + secondAttack.value + thirdAttack.value + fourthAttack.value + fifthAttack.value + sixthAttack.value + seventhAttack.value + eighthAttack.value + ninthAttack.value;
    attackTime = (Math.floor(attackTime * 100)) / 100;
    return attackTime;
  }
)
const cumulativeTenthAttack = computed(
  (): number => {
    let attackTime = firstAttack.value + secondAttack.value + thirdAttack.value + fourthAttack.value + fifthAttack.value + sixthAttack.value + seventhAttack.value + eighthAttack.value + ninthAttack.value + tenthAttack.value;
    attackTime = (Math.floor(attackTime * 100)) / 100;
    return attackTime;
  }
)
const cumulativeEleventhAttack = computed(
  (): number => {
    let attackTime = firstAttack.value + secondAttack.value + thirdAttack.value + fourthAttack.value + fifthAttack.value + sixthAttack.value + seventhAttack.value + eighthAttack.value + ninthAttack.value + tenthAttack.value + eleventhAttack.value;
    attackTime = (Math.floor(attackTime * 100)) / 100;
    return attackTime;
  }
)
const cumulativeTwelfthAttack = computed(
  (): number => {
    let attackTime = firstAttack.value + secondAttack.value + thirdAttack.value + fourthAttack.value + fifthAttack.value + sixthAttack.value + seventhAttack.value + eighthAttack.value + ninthAttack.value + tenthAttack.value + eleventhAttack.value + twelfthAttack.value;
        attackTime = (Math.floor(attackTime * 100)) / 100;
    return attackTime;
  }
)
</script>

<template>
    <h3>フリードリヒ・デア・グローセ</h3>
  装備の基本攻速(装備をキャラから外した状態で見てください)
  <input type="number" step="0.01" v-model.number="defaultRateOfFire">s
  <br>
  <br>
  素の装填値
  <input type="number" v-model.number="defaultReload">
  装備の装填値
  <input type="number" v-model.number="equipmentReload">
  艦船技術の装填値
  <input type="number" v-model.number="fleetTechnology">
  オフニャの装填値
  <input type="number" v-model.number="meowfficer">
  <br>
  <br>
  混沌のSonate
  <input type="number" v-model.number="sonataOfChaos">%
  <br>
  <br>
  装填上昇スキル1
  <input type="number" v-model.number="skill1">%
  装填上昇スキル2
  <input type="number" v-model.number="skill2">%
  装填上昇スキル3
  <input type="number" v-model.number="skill3">%
  <br>
  <br>
  高性能火器管制レーダーまたはアドミラルティ射撃統制システム<input type="checkbox" v-model="highPeformanceFireControllRader">  <br>
  【試作砲身】(試作型406mm連装砲Mk4)自身の5回目以降の主砲攻撃の装填時間が35%長くなる<input type="checkbox" v-model="experimentalGunBarrel">
  <hr>
攻速(1回目):{{ firstAttack }} 攻速(2回目):{{ secondAttack }} 攻速(3回目):{{ thirdAttack }} 攻速(4回目):{{ fourthAttack }} 攻速(5回目):{{ fifthAttack }} 攻速(6回目):{{ sixthAttack }} 攻速(7回目):{{ seventhAttack }} 攻速(8回目):{{ eighthAttack }} 攻速(9回目):{{ ninthAttack }} 攻速(10回目):{{ tenthAttack }} 攻速(11回目):{{ eleventhAttack }} 攻速(12回目):{{ twelfthAttack }}
<br>
攻撃1回目:{{ firstAttack }}s<br>
攻撃2回目:{{ cumulativeSecondAttack }}s<br>
攻撃3回目:{{ cumulativeThirdAttack }}s<br>
攻撃4回目:{{ cumulativeFourthAttack }}s<br>
攻撃5回目:{{ cumulativeFifthAttack }}s<br>
攻撃6回目:{{ cumulativeSixthAttack }}s<br>
攻撃7回目:{{ cumulativeSeventhAttack }}s<br>
攻撃8回目:{{ cumulativeEighthAttack}}s<br>
攻撃9回目:{{ cumulativeNinthAttack }}s<br>
攻撃10回目:{{ cumulativeTenthAttack }}s<br>
攻撃11回目:{{ cumulativeEleventhAttack }}s<br>
攻撃12回目:{{ cumulativeTwelfthAttack }}s<br>

</template>

<style>

input[type="number"] {
  width: 60px;
}
</style>