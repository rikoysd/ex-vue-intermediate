<template>
  <div>
    <div class="list">球団名</div>
    {{ currentTeam.teamName }}
    <div class="list">本拠地</div>
    {{ currentTeam.headquarters }}
    <div class="list">発足日</div>
    {{ currentTeam.formatString }}
    <div class="list">歴史</div>
    {{ currentTeam.history }}
    <button type="button" v-on:click="onclick">戻る</button>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";
import { Team } from "@/types/Team";
@Component
export default class BaseballTeamDetail extends Vue {
  private currentTeam = new Team(0, "", "", new Date(), "");
  /**
   * 戻るボタンを押すとチーム一覧に遷移する.
   */
  onclick(): void {
    this.$router.push("/baseballTeamList");
  }
}
</script>

<style scoped></style>
