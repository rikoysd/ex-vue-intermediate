<template>
  <div>
    <div class="list">球団名</div>
    {{ team.teamName }}
    <div class="list">本拠地</div>
    {{ team.headquarters }}
    <div class="list">発足日</div>
    <div class="list">歴史</div>
    {{ team.history }}
  </div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";
import { Team } from "@/types/Team";
import { Hotel } from "@/types/Hotel";
import { Clothe } from "@/types/Clothe";
@Component
export default class BaseballTeamDetail extends Vue {}
</script>

<style scoped></style>
