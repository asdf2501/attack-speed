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
const skill4 = ref(0);
const skill5 = ref(0);
const skill6 = ref(0);

const directReductionSkill1 = ref(0);
const directReductionSkill2 = ref(0);
const directReductionSkill3 = ref(0);

const oneTimeDirectReductionSkill = ref(0);
const upToSecondDirectReductionSkill = ref(0);
const upToThirdDirectReductionSkill = ref(0);
const upToFourthDirectReductionSkill = ref(0);

const highPeformanceFireControllRader = ref(false);
const experimentalGunBarrel = ref(false);

const firstAttack = computed(
  (): number => {
    let attackTime = ( defaultRateOfFire.value * Math.sqrt( 200 / ( 100 + ( defaultReload.value + equipmentReload.value + fleetTechnology.value + meowfficer.value ) * (1 + skill1.value/100 + skill2.value/100 + skill3.value/100 + skill4.value/100 + skill5.value/100 + skill6.value/100))) * ( 1 - ( directReductionSkill1.value/100 + directReductionSkill2.value/100 + directReductionSkill3.value/100 + oneTimeDirectReductionSkill.value/100 + upToSecondDirectReductionSkill.value/100 + upToThirdDirectReductionSkill.value/100 + upToFourthDirectReductionSkill.value/100)));
    if(highPeformanceFireControllRader.value){
      attackTime = attackTime * 0.85;
    }
    attackTime = (Math.ceil(attackTime * 100)) / 100;
    return attackTime;
  }
)
const secondAttack = computed(
  (): number => {
    let attackTime = ( defaultRateOfFire.value * Math.sqrt( 200 / ( 100 + ( defaultReload.value + equipmentReload.value + fleetTechnology.value + meowfficer.value ) * (1 + skill1.value/100 + skill2.value/100 + skill3.value/100 + skill4.value/100 + skill5.value/100 + skill6.value/100))) * ( 1 - ( directReductionSkill1.value/100 + directReductionSkill2.value/100 + directReductionSkill3.value/100 + upToSecondDirectReductionSkill.value/100 + upToThirdDirectReductionSkill.value/100 + upToFourthDirectReductionSkill.value/100)));
    attackTime = (Math.ceil(attackTime * 100)) / 100;
    return attackTime;
  }
)
const thirdAttack = computed(
  (): number => {
    let attackTime = ( defaultRateOfFire.value * Math.sqrt( 200 / ( 100 + ( defaultReload.value + equipmentReload.value + fleetTechnology.value +meowfficer.value ) * (1 + skill1.value/100 + skill2.value/100 + skill3.value/100 + skill4.value/100 + skill5.value/100 + skill6.value/100))) * ( 1 - ( directReductionSkill1.value/100 + directReductionSkill2.value/100 + directReductionSkill3.value/100 + upToThirdDirectReductionSkill.value/100 + upToFourthDirectReductionSkill.value/100)));
    attackTime = (Math.ceil(attackTime * 100)) / 100;
    return attackTime;
  }
)
const fourthAttack = computed(
  (): number => {
    let attackTime = ( defaultRateOfFire.value * Math.sqrt( 200 / ( 100 + ( defaultReload.value + equipmentReload.value + fleetTechnology.value + meowfficer.value ) * (1 + skill1.value/100 + skill2.value/100 + skill3.value/100 + skill4.value/100 + skill5.value/100 + skill6.value/100))) * ( 1 - ( directReductionSkill1.value/100 + directReductionSkill2.value/100 + directReductionSkill3.value/100 + upToFourthDirectReductionSkill.value/100)));
    attackTime = (Math.ceil(attackTime * 100)) / 100;
    return attackTime;
  }
)
const fifthAttack = computed(
  (): number => {
    let attackTime = ( defaultRateOfFire.value * Math.sqrt( 200 / ( 100 + ( defaultReload.value + equipmentReload.value + fleetTechnology.value + meowfficer.value ) * (1 + skill1.value/100 + skill2.value/100 + skill3.value/100 + skill4.value/100 + skill5.value/100 + skill6.value/100))) * ( 1 - ( directReductionSkill1.value/100 + directReductionSkill2.value/100 + directReductionSkill3.value/100)));
    if(experimentalGunBarrel.value) {
      attackTime = attackTime * 1.35;
    }
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
    let attackTime = firstAttack.value + secondAttack.value + thirdAttack.value + fourthAttack.value;
    attackTime = (Math.ceil(attackTime * 100)) / 100;
    return attackTime;
  }
)
const cumulativeFifthAttack = computed(
  (): number => {
    let attackTime = firstAttack.value + secondAttack.value + thirdAttack.value + fourthAttack.value + fifthAttack.value;
    attackTime = (Math.ceil(attackTime * 100)) / 100;
    return attackTime;
  }
)
const cumulativeSixthAttack = computed(
  (): number => {
    let attackTime = firstAttack.value + secondAttack.value + thirdAttack.value + fourthAttack.value + fifthAttack.value*2;
    attackTime = (Math.ceil(attackTime * 100)) / 100;
    return attackTime;
  }
)
const cumulativeSeventhAttack = computed(
  (): number => {
    let attackTime = firstAttack.value + secondAttack.value + thirdAttack.value + fourthAttack.value + fifthAttack.value*3;
    attackTime = (Math.ceil(attackTime * 100)) / 100;
    return attackTime;
  }
)
const cumulativeEighthAttack = computed(
  (): number => {
    let attackTime = firstAttack.value + secondAttack.value + thirdAttack.value + fourthAttack.value + fifthAttack.value*4;
    attackTime = (Math.ceil(attackTime * 100)) / 100;
    return attackTime;
  }
)
const cumulativeNinthAttack = computed(
  (): number => {
    let attackTime = firstAttack.value + secondAttack.value + thirdAttack.value + fourthAttack.value + fifthAttack.value*5;
    attackTime = (Math.ceil(attackTime * 100)) / 100;
    return attackTime;
  }
)
const cumulativeTenthAttack = computed(
  (): number => {
    let attackTime = firstAttack.value + secondAttack.value + thirdAttack.value + fourthAttack.value + fifthAttack.value*6;
    attackTime = (Math.ceil(attackTime * 100)) / 100;
    return attackTime;
  }
)
const cumulativeEleventhAttack = computed(
  (): number => {
    let attackTime = firstAttack.value + secondAttack.value + thirdAttack.value + fourthAttack.value + fifthAttack.value*7;
    attackTime = (Math.ceil(attackTime * 100)) / 100;
    return attackTime;
  }
)
const cumulativeTwelfthAttack = computed(
  (): number => {
    let attackTime = firstAttack.value + secondAttack.value + thirdAttack.value + fourthAttack.value + fifthAttack.value*8;
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
  オフニャの装填値
  <input type="number" v-model.number="meowfficer">
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
  直接短縮スキル1(ウルリッヒフォンフッテンなど)
  <input type="number" v-model.number="directReductionSkill1">%
  直接短縮スキル2
  <input type="number" v-model.number="directReductionSkill2">%
  直接短縮スキル3
  <input type="number" v-model.number="directReductionSkill3">%
  <br>
  <br>
  1回目のみの直接短縮スキル(プリンス・オブ・ウェールズなど)
  <input type="number" v-model.number="oneTimeDirectReductionSkill">%<br>
  2回目までの直接短縮スキル(レナウン(META)など)
  <input type="number" v-model.number="upToSecondDirectReductionSkill">%<br>
  3回目までの直接短縮スキル(リトル・レナウンなど)
  <input type="number" v-model.number="upToThirdDirectReductionSkill">%<br>
  4回目までの直接短縮スキル(ガングートなど)
  <input type="number" v-model.number="upToFourthDirectReductionSkill">%
  <br>
  <br>
  高性能火器管制レーダーまたはアドミラルティ射撃統制システム<input type="checkbox" v-model="highPeformanceFireControllRader">  <br>
  【試作砲身】(試作型406mm連装砲Mk4)自身の5回目以降の主砲攻撃の装填時間が35%長くなる<input type="checkbox" v-model="experimentalGunBarrel">
  <hr>
攻速(1回目):{{ firstAttack }} 攻速(2回目):{{ secondAttack }} 攻速(3回目):{{ thirdAttack }} 攻速(4回目):{{ fourthAttack }} 攻速(5回目以降):{{ fifthAttack }}
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