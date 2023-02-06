<script setup lang="ts">
import {ref} from "vue";

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
const upTo2ndDirectReductionSkill = ref(0);
const upTo3rdDirectReductionSkill = ref(0);

const highPeformanceFireControllRader = ref(false);

const firstAttack = ref( defaultRateOfFire );
const secondAttack = ref();
const thirdAttack = ref();
const fourthAttack = ref();

</script>
<template>
  装備の基本攻速
  <input type="number" v-model="defaultRateOfFire">
  <br>
  <br>
  素の装填値
  <input type="number" v-model="defaultReload">
  装備の装填値
  <input type="number" v-model="equipmentReload">
  艦船技術の装填値
  <input type="number" v-model="fleetTechnology">
  <br>
  <br>
  装填上昇スキル1
  <input type="number" v-model="skill1">%
  装填上昇スキル2
  <input type="number" v-model="skill2">%
  装填上昇スキル3
  <input type="number" v-model="skill3">%
  <br>
  装填上昇スキル4
  <input type="number" v-model="skill4">%
  装填上昇スキル5
  <input type="number" v-model="skill5">%
  装填上昇スキル6
  <input type="number" v-model="skill6">%
  <br>
  <br>
  直接短縮スキル1
  <input type="number" v-model="directReductionSkill1">%
  直接短縮スキル2
  <input type="number" v-model="directReductionSkill2">%
  直接短縮スキル3
  <input type="number" v-model="directReductionSkill3">%
  <br>
  <br>
  1回目のみの直接短縮スキル
  <input type="number" v-model="oneTimeDirectReductionSkill">%
  2回目までの直接短縮スキル
  <input type="number" v-model="upTo2ndDirectReductionSkill">%
  3回目までの直接短縮スキル
  <input type="number" v-model="upTo3rdDirectReductionSkill">%
  <br>
  <br>
  高性能火器管制レーダーまたはアドミラルティ射撃統制システム<input type="checkbox" v-model="highPeformanceFireControllRader">
  <hr>

</template>

<style>
input[type="number"] {
  width: 35px;
}
</style>