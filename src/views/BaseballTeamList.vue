<template>
  <div class="container">
    <h1>野球チーム一覧</h1>
    <table>
      <tr v-for="team of getteams" v-bind:key="team.id">
        <router-link :to="'/baseballTeamDetail' + team.id">{{
          team.teamName
        }}</router-link>
      </tr>
    </table>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";
import { Team } from "@/types/Team";
@Component
export default class BaseballTeamList extends Vue {
  /**
   * Vuexストア内のチーム一覧を取得し返す.
   * @returns チーム一覧
   */
  get getteams(): Array<Team> {
    return this.$store.getters.getteams;
  }
}
</script>

<style scoped>
.container {
  text-align: left;
}
</style>
