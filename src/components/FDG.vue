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
    <h3>??????????????????????????????????????????</h3>
  ?????????????????????(????????????????????????????????????????????????????????????)
  <input type="number" step="0.01" v-model.number="defaultRateOfFire">s
  <br>
  <br>
  ???????????????
  <input type="number" v-model.number="defaultReload">
  ??????????????????
  <input type="number" v-model.number="equipmentReload">
  ????????????????????????
  <input type="number" v-model.number="fleetTechnology">
  ????????????????????????
  <input type="number" v-model.number="meowfficer">
  <br>
  <br>
  ?????????Sonate
  <input type="number" v-model.number="sonataOfChaos">%
  <br>
  <br>
  ?????????????????????1
  <input type="number" v-model.number="skill1">%
  ?????????????????????2
  <input type="number" v-model.number="skill2">%
  ?????????????????????3
  <input type="number" v-model.number="skill3">%
  <br>
  <br>
  ???????????????????????????????????????????????????????????????????????????????????????<input type="checkbox" v-model="highPeformanceFireControllRader">  <br>
  ??????????????????(?????????406mm?????????Mk4)?????????5?????????????????????????????????????????????35%????????????<input type="checkbox" v-model="experimentalGunBarrel">
  <hr>
??????(1??????):{{ firstAttack }} ??????(2??????):{{ secondAttack }} ??????(3??????):{{ thirdAttack }} ??????(4??????):{{ fourthAttack }} ??????(5??????):{{ fifthAttack }} ??????(6??????):{{ sixthAttack }} ??????(7??????):{{ seventhAttack }} ??????(8??????):{{ eighthAttack }} ??????(9??????):{{ ninthAttack }} ??????(10??????):{{ tenthAttack }} ??????(11??????):{{ eleventhAttack }} ??????(12??????):{{ twelfthAttack }}
<br>
??????1??????:{{ firstAttack }}s<br>
??????2??????:{{ cumulativeSecondAttack }}s<br>
??????3??????:{{ cumulativeThirdAttack }}s<br>
??????4??????:{{ cumulativeFourthAttack }}s<br>
??????5??????:{{ cumulativeFifthAttack }}s<br>
??????6??????:{{ cumulativeSixthAttack }}s<br>
??????7??????:{{ cumulativeSeventhAttack }}s<br>
??????8??????:{{ cumulativeEighthAttack}}s<br>
??????9??????:{{ cumulativeNinthAttack }}s<br>
??????10??????:{{ cumulativeTenthAttack }}s<br>
??????11??????:{{ cumulativeEleventhAttack }}s<br>
??????12??????:{{ cumulativeTwelfthAttack }}s<br>

</template>

<style>

input[type="number"] {
  width: 60px;
}
</style>