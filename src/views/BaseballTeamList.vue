<template>
  <div>
    <h1>野球チーム一覧</h1>
    <div>
      <router-link>読売ジャイアンツ</router-link>
      <router-link>阪神タイガース</router-link>
      <router-link>中日ドラゴンズ</router-link>
      <router-link>横浜DeNAベイスターズ</router-link>
      <router-link>広島東洋カープ</router-link>
      <router-link>東京ヤクルトスワローズ</router-link>
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";
@Component
export default class BaseballTeamList extends Vue {
  

}
</script>

<style scoped>

</style>