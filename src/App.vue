<script setup lang="ts">
import {ref, computed} from "vue";

const defaultRateOfFire = ref(0);

const defaultReload = ref(0);
const equipmentReload = ref(0);
const fleetTechnology = ref(0);

const skill1 = ref(0);
const skill2 = ref(0);
const skill3 = ref(0);
const skill4 = ref(0);
const skill5 = ref(0);
const skill6 = ref(0);

const directReductionSkill1 = ref(0);
const directReductionSkill2 = ref(0);
const directReductionSkill3 = ref(0);

const oneTimeDirectReductionSkill = ref(0);
const upToSecondDirectReductionSkill = ref(0);
const upToThirdDirectReductionSkill = ref(0);

const highPeformanceFireControllRader = ref(false);

const firstAttack = computed(
  (): number => {
    let attackTime = ( defaultRateOfFire.value * Math.sqrt( 200 / (( 100 + defaultReload.value + equipmentReload.value + fleetTechnology.value ) * (1 + skill1.value/100 + skill2.value/100 + skill3.value/100 + skill4.value/100 + skill5.value/100 + skill6.value/100))) * ( 1 - ( directReductionSkill1.value/100 + directReductionSkill2.value/100 + directReductionSkill3.value/100 + oneTimeDirectReductionSkill.value/100 + upToSecondDirectReductionSkill.value/100 + upToThirdDirectReductionSkill.value/100)));
    if(highPeformanceFireControllRader.value){
      attackTime = attackTime * 0.85;
    }
    attackTime = (Math.ceil(attackTime * 100)) / 100;
    return attackTime;
  }
)
const secondAttack = computed(
  (): number => {
    let attackTime = ( defaultRateOfFire.value * Math.sqrt( 200 / (( 100 + defaultReload.value + equipmentReload.value + fleetTechnology.value ) * (1 + skill1.value/100 + skill2.value/100 + skill3.value/100 + skill4.value/100 + skill5.value/100 + skill6.value/100))) * ( 1 - ( directReductionSkill1.value/100 + directReductionSkill2.value/100 + directReductionSkill3.value/100 + upToSecondDirectReductionSkill.value/100 + upToThirdDirectReductionSkill.value/100)));
    attackTime = (Math.ceil(attackTime * 100)) / 100;
    return attackTime;
  }
)
const thirdAttack = computed(
  (): number => {
    let attackTime = ( defaultRateOfFire.value * Math.sqrt( 200 / (( 100 + defaultReload.value + equipmentReload.value + fleetTechnology.value ) * (1 + skill1.value/100 + skill2.value/100 + skill3.value/100 + skill4.value/100 + skill5.value/100 + skill6.value/100))) * ( 1 - ( directReductionSkill1.value/100 + directReductionSkill2.value/100 + directReductionSkill3.value/100 + upToThirdDirectReductionSkill.value/100)));
    attackTime = (Math.ceil(attackTime * 100)) / 100;
    return attackTime;
  }
)
const fourthTimeOnwardsAttack = computed(
  (): number => {
    let attackTime = ( defaultRateOfFire.value * Math.sqrt( 200 / (( 100 + defaultReload.value + equipmentReload.value + fleetTechnology.value ) * (1 + skill1.value/100 + skill2.value/100 + skill3.value/100 + skill4.value/100 + skill5.value/100 + skill6.value/100))) * ( 1 - ( directReductionSkill1.value/100 + directReductionSkill2.value/100 + directReductionSkill3.value/100)));
    attackTime = (Math.ceil(attackTime * 100)) / 100;
    return attackTime;
  }
)
const cumulativeSecondAttack = computed(
  (): number => {
    let attackTime = firstAttack.value + secondAttack.value;
    attackTime = (Math.ceil(attackTime * 100)) / 100;
    return attackTime;
  }
)
const cumulativeThirdAttack = computed(
  (): number => {
    let attackTime = firstAttack.value + secondAttack.value + thirdAttack.value;
    attackTime = (Math.ceil(attackTime * 100)) / 100;
    return attackTime;
  }
)
const cumulativeFourthAttack = computed(
  (): number => {
    let attackTime = firstAttack.value + secondAttack.value + thirdAttack.value + fourthTimeOnwardsAttack.value;
    attackTime = (Math.ceil(attackTime * 100)) / 100;
    return attackTime;
  }
)
const cumulativeFifthAttack = computed(
  (): number => {
    let attackTime = firstAttack.value + secondAttack.value + thirdAttack.value + fourthTimeOnwardsAttack.value*2;
    attackTime = (Math.ceil(attackTime * 100)) / 100;
    return attackTime;
  }
)
const cumulativeSixthAttack = computed(
  (): number => {
    let attackTime = firstAttack.value + secondAttack.value + thirdAttack.value + fourthTimeOnwardsAttack.value*3;
    attackTime = (Math.ceil(attackTime * 100)) / 100;
    return attackTime;
  }
)
</script>

<template>
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
  <br>
  <br>
  装填上昇スキル1
  <input type="number" v-model.number="skill1">%
  装填上昇スキル2
  <input type="number" v-model.number="skill2">%
  装填上昇スキル3
  <input type="number" v-model.number="skill3">%
  <br>
  装填上昇スキル4
  <input type="number" v-model.number="skill4">%
  装填上昇スキル5
  <input type="number" v-model.number="skill5">%
  装填上昇スキル6
  <input type="number" v-model.number="skill6">%
  <br>
  <br>
  直接短縮スキル1
  <input type="number" v-model.number="directReductionSkill1">%
  直接短縮スキル2
  <input type="number" v-model.number="directReductionSkill2">%
  直接短縮スキル3
  <input type="number" v-model.number="directReductionSkill3">%
  <br>
  <br>
  1回目のみの直接短縮スキル
  <input type="number" v-model.number="oneTimeDirectReductionSkill">%
  2回目までの直接短縮スキル
  <input type="number" v-model.number="upToSecondDirectReductionSkill">%
  3回目までの直接短縮スキル
  <input type="number" v-model.number="upToThirdDirectReductionSkill">%
  <br>
  <br>
  高性能火器管制レーダーまたはアドミラルティ射撃統制システム<input type="checkbox" v-model="highPeformanceFireControllRader">
  <hr>
攻速(1回目):{{ firstAttack }} 攻速(2回目):{{ secondAttack }} 攻速(3回目):{{ thirdAttack }} 攻速(4回目以降):{{ fourthTimeOnwardsAttack }}
<br>
攻撃1回目:{{ firstAttack }}<br>
攻撃2回目:{{ cumulativeSecondAttack }}<br>
攻撃3回目:{{ cumulativeThirdAttack }}<br>
攻撃4回目:{{ cumulativeFourthAttack }}<br>
攻撃5回目:{{ cumulativeFifthAttack }}<br>
攻撃6回目:{{ cumulativeSixthAttack }}<br>


</template>

<style>
input[type="number"] {
  width: 60px;
}
</style>