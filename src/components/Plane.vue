<script setup lang="ts">
import {ref, computed} from "vue";

const defaultReloadSpeed1 = ref(0);
const defaultReloadSpeed2 = ref(0);
const defaultReloadSpeed3 = ref(0);

const numberOfPlane1 = ref(1);
const numberOfPlane2 = ref(0);
const numberOfPlane3 = ref(0);

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

const bisyamaru = ref(false);
const bisyamaruSikihojo = ref(161);
const hangekikedamakenLv3 =ref(false);

const homingBeacon = ref(false);
const eliteAviationMaintenanceManjuu = ref(false);

const hangekikedamakenLv1 = computed(
  (): number => {
    let correction = 0.8 * bisyamaruSikihojo.value / 100 ;
    if(bisyamaru.value){return correction}
    else {return 0};
  }
)

const attackSpeedOfPlane1 = computed(
    (): number => {
        let attackTime =  defaultReloadSpeed1.value * Math.sqrt( 200 / ( 100 + ( defaultReload.value + equipmentReload.value + fleetTechnology.value + meowfficer.value ) * (1 + skill1.value/100 + skill2.value/100 + skill3.value/100 + skill4.value/100 + skill5.value/100 + skill6.value/100 + hangekikedamakenLv1.value/100)));
        return attackTime;
    }
)
const attackSpeedOfPlane2 = computed(
    (): number => {
        let attackTime =  defaultReloadSpeed2.value * Math.sqrt( 200 / ( 100 + ( defaultReload.value + equipmentReload.value + fleetTechnology.value + meowfficer.value ) * (1 + skill1.value/100 + skill2.value/100 + skill3.value/100 + skill4.value/100 + skill5.value/100 + skill6.value/100 + hangekikedamakenLv1.value/100)));
        return attackTime;
    }
)
const attackSpeedOfPlane3 = computed(
    (): number => {
        let attackTime =  defaultReloadSpeed3.value * Math.sqrt( 200 / ( 100 + ( defaultReload.value + equipmentReload.value + fleetTechnology.value + meowfficer.value ) * (1 + skill1.value/100 + skill2.value/100 + skill3.value/100 + skill4.value/100 + skill5.value/100 + skill6.value/100 + hangekikedamakenLv1.value/100)));
        return attackTime;
    }
)

const firstAttackSpeedOfPlane1 = computed(
    (): number => {
        let attackTime = 0;
        if(bisyamaru.value && hangekikedamakenLv3.value) {attackTime = defaultReloadSpeed1.value * Math.sqrt( 200 / ( 100 + ( defaultReload.value + equipmentReload.value + fleetTechnology.value + meowfficer.value ) * (1 + skill1.value/100 + skill2.value/100 + skill3.value/100 + skill4.value/100 + skill5.value/100 + skill6.value/100 + hangekikedamakenLv1.value/100 + 8/100)))}
        else{ attackTime = defaultReloadSpeed1.value * Math.sqrt( 200 / ( 100 + ( defaultReload.value + equipmentReload.value + fleetTechnology.value + meowfficer.value ) * (1 + skill1.value/100 + skill2.value/100 + skill3.value/100 + skill4.value/100 + skill5.value/100 + skill6.value/100 + hangekikedamakenLv1.value/100)))};
        return attackTime;
    }
)
const firstAttackSpeedOfPlane2 = computed(
    (): number => {
        let attackTime = 0;
        if(bisyamaru.value && hangekikedamakenLv3.value){attackTime = defaultReloadSpeed2.value * Math.sqrt( 200 / ( 100 + ( defaultReload.value + equipmentReload.value + fleetTechnology.value + meowfficer.value ) * (1 + skill1.value/100 + skill2.value/100 + skill3.value/100 + skill4.value/100 + skill5.value/100 + skill6.value/100 + hangekikedamakenLv1.value/100 + 8/100)))}
        else{attackTime = defaultReloadSpeed2.value * Math.sqrt( 200 / ( 100 + ( defaultReload.value + equipmentReload.value + fleetTechnology.value + meowfficer.value ) * (1 + skill1.value/100 + skill2.value/100 + skill3.value/100 + skill4.value/100 + skill5.value/100 + skill6.value/100 + hangekikedamakenLv1.value/100)))};
        return attackTime;
    }
)
const firstAttackSpeedOfPlane3 = computed(
    (): number => {
      let attackTime = 0;
        if(bisyamaru.value && hangekikedamakenLv3.value){attackTime = defaultReloadSpeed3.value * Math.sqrt( 200 / ( 100 + ( defaultReload.value + equipmentReload.value + fleetTechnology.value + meowfficer.value ) * (1 + skill1.value/100 + skill2.value/100 + skill3.value/100 + skill4.value/100 + skill5.value/100 + skill6.value/100 + hangekikedamakenLv1.value/100+ 8/100)))}
        else{attackTime = defaultReloadSpeed2.value * Math.sqrt( 200 / ( 100 + ( defaultReload.value + equipmentReload.value + fleetTechnology.value + meowfficer.value ) * (1 + skill1.value/100 + skill2.value/100 + skill3.value/100 + skill4.value/100 + skill5.value/100 + skill6.value/100 + hangekikedamakenLv1.value/100)))};
        return attackTime;
    }
)

const firstAttack = computed(
    (): number => {
        let attackTime = (( firstAttackSpeedOfPlane1.value * numberOfPlane1.value + firstAttackSpeedOfPlane2.value * numberOfPlane2.value + firstAttackSpeedOfPlane3.value * numberOfPlane3.value) *2.2 / (numberOfPlane1.value + numberOfPlane2.value + numberOfPlane3.value) + 0.01 ) * ( 1 - ( directReductionSkill1.value/100 + directReductionSkill2.value/100 + directReductionSkill3.value/100 + oneTimeDirectReductionSkill.value + upToSecondDirectReductionSkill.value/100 + upToThirdDirectReductionSkill.value/100));
        if(homingBeacon.value && eliteAviationMaintenanceManjuu.value){}
        else if(homingBeacon.value){
            attackTime = attackTime * 0.96;
        }
        else if(eliteAviationMaintenanceManjuu.value){
            attackTime = attackTime * 1.04;
        }
        attackTime = (Math.floor(attackTime * 100)) / 100;
        return attackTime;
    }
)
const secondAttack = computed(
    (): number => {
        let attackTime = (( attackSpeedOfPlane1.value * numberOfPlane1.value + attackSpeedOfPlane2.value * numberOfPlane2.value + attackSpeedOfPlane3.value * numberOfPlane3.value) *2.2 / (numberOfPlane1.value + numberOfPlane2.value + numberOfPlane3.value) + 0.01 ) * ( 1 - ( directReductionSkill1.value/100 + directReductionSkill2.value/100 + directReductionSkill3.value/100 + upToSecondDirectReductionSkill.value/100 + upToThirdDirectReductionSkill.value/100));
        if(homingBeacon.value && eliteAviationMaintenanceManjuu.value){}
        else if(homingBeacon.value){
            attackTime = attackTime * 0.96;
        }
        else if(eliteAviationMaintenanceManjuu.value){
            attackTime = attackTime * 1.04;
        }
        attackTime = (Math.floor(attackTime * 100)) / 100;
        return attackTime;
    }
)
const thirdAttack = computed(
    (): number => {
        let attackTime = (( attackSpeedOfPlane1.value * numberOfPlane1.value + attackSpeedOfPlane2.value * numberOfPlane2.value + attackSpeedOfPlane3.value * numberOfPlane3.value) *2.2 / (numberOfPlane1.value + numberOfPlane2.value + numberOfPlane3.value) + 0.01 ) * ( 1 - ( directReductionSkill1.value/100 + directReductionSkill2.value/100 + directReductionSkill3.value/100 + upToThirdDirectReductionSkill.value/100));
        if(homingBeacon.value && eliteAviationMaintenanceManjuu.value){}
        else if(homingBeacon.value){
            attackTime = attackTime * 0.96;
        }
        else if(eliteAviationMaintenanceManjuu.value){
            attackTime = attackTime * 1.04;
        }
        attackTime = (Math.floor(attackTime * 100)) / 100;
        return attackTime;
    }
)
const fourthAttack = computed(
    (): number => {
        let attackTime = (( attackSpeedOfPlane1.value * numberOfPlane1.value + attackSpeedOfPlane2.value * numberOfPlane2.value + attackSpeedOfPlane3.value * numberOfPlane3.value) *2.2 / (numberOfPlane1.value + numberOfPlane2.value + numberOfPlane3.value) + 0.01 ) * ( 1 - ( directReductionSkill1.value/100 + directReductionSkill2.value/100 + directReductionSkill3.value/100));
        if(homingBeacon.value && eliteAviationMaintenanceManjuu.value){}
        else if(homingBeacon.value){
            attackTime = attackTime * 0.96;
        }
        else if(eliteAviationMaintenanceManjuu.value){
            attackTime = attackTime * 1.04;
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
    let attackTime = firstAttack.value + secondAttack.value + thirdAttack.value + fourthAttack.value*2;
    attackTime = (Math.floor(attackTime * 100)) / 100;
    return attackTime;
  }
)
const cumulativeSixthAttack = computed(
  (): number => {
    let attackTime = firstAttack.value + secondAttack.value + thirdAttack.value + fourthAttack.value*3;
    attackTime = (Math.floor(attackTime * 100)) / 100;
    return attackTime;
  }
)
</script>

<template>
    <h3>航空</h3>
    (装備をキャラから外した状態で見てください)<br>
    艦載機1の基本攻速
    <input type="number" step="0.01" v-model.number="defaultReloadSpeed1">s
    艦載機1の機数
    <input type="number" v-model.number="numberOfPlane1"><br>
    艦載機2の基本攻速
    <input type="number" step="0.01" v-model.number="defaultReloadSpeed2">s
    艦載機2の機数
    <input type="number" v-model.number="numberOfPlane2"><br>
    艦載機3の基本攻速
    <input type="number" step="0.01" v-model.number="defaultReloadSpeed3">s
    艦載機3の機数
    <input type="number" v-model.number="numberOfPlane3">
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
    
    直接短縮スキル:アクィラ(爆撃機装備時の開幕航空以外10%)など。パーシュースは-90%と入力してください。<br>
    直接短縮スキル1
    <input type="number" v-model.number="directReductionSkill1">%
    直接短縮スキル2
    <input type="number" v-model.number="directReductionSkill2">%
    直接短縮スキル3
    <input type="number" v-model.number="directReductionSkill3">%
    <br>
    <br>
    1回目のみの直接短縮スキル(赤城・加賀(空母)など)
    <input type="number" v-model.number="oneTimeDirectReductionSkill">%<br>
    2回目までの直接短縮スキル(伊勢改など)
    <input type="number" v-model.number="upToSecondDirectReductionSkill">%<br>
    3回目までの直接短縮スキル(ペーター・シュトラッサーなど)
    <input type="number" v-model.number="upToThirdDirectReductionSkill">%<br>
   <br>
    ホーミングビーコン
    <input type="checkbox" v-model="homingBeacon">
    <br>
    精鋭航空整備饅頭
    <input type="checkbox" v-model="eliteAviationMaintenanceManjuu">
    <br>
    オフニャ：ビシャマル
    <input type="checkbox" v-model="bisyamaru">
    ビシャマルの指揮補助
    <input type="number" v-model.number="bisyamaruSikihojo">反撃毛玉拳Lv1の効果:{{ hangekikedamakenLv1 }}%
    反撃毛玉拳Lv3
    <input type="checkbox" v-model="hangekikedamakenLv3">
    <hr>
    攻速(1回目):{{ firstAttack }} 攻速(2回目):{{ secondAttack }} 攻速(3回目):{{ thirdAttack }} 攻速(4回目以降):{{ fourthAttack }}
    <br>
    攻撃1回目:{{ firstAttack }}s<br>
    攻撃2回目:{{ cumulativeSecondAttack }}s<br>
    攻撃3回目:{{ cumulativeThirdAttack }}s<br>
    攻撃4回目:{{ cumulativeFourthAttack }}s<br>
    攻撃5回目:{{ cumulativeFifthAttack }}s<br>
    攻撃6回目:{{ cumulativeSixthAttack }}s<br>
</template>

<style>
input[type="number"] {
  width: 60px;
}
</style>