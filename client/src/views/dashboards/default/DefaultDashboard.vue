<script setup lang="ts">
// imported components
// import TotalEarning from './components/TotalEarning.vue';
// import TotalOrder from './components/TotalOrder.vue';
// import TotalIncome from './components/TotalIncome.vue';
// import TotalGrowth from './components/TotalGrowth.vue';
// import PopularStocks from './components/PopularStocks.vue';
</script>

<template>
  <div class="safety-banner">
    <div class="safety-text">
      <p><strong>작업의 기본은 안전,</strong></p>
      <p><strong>완성의 핵심은 디테일</strong></p>
    </div>
    <img src="@/assets/images/logos/gg.svg" alt="공작이" class="gongjaki" />
  </div>
  <!-- <v-row> -->
  <!-- -------------------------------------------------------------------- -->
  <!-- Total Earning -->
  <!-- -------------------------------------------------------------------- -->
  <!-- <v-col cols="12" md="4">
      <TotalEarning />
    </v-col> -->
  <!-- -------------------------------------------------------------------- -->
  <!-- Total Order -->
  <!-- -------------------------------------------------------------------- -->
  <!-- <v-col cols="12" md="4">
      <TotalOrder />
    </v-col> -->
  <!-- -------------------------------------------------------------------- -->
  <!-- Total Income -->
  <!-- -------------------------------------------------------------------- -->
  <!-- <v-col cols="12" md="4">
      <TotalIncome />
    </v-col> -->

  <!-- -------------------------------------------------------------------- -->
  <!-- Total Growth -->
  <!-- -------------------------------------------------------------------- -->
  <!-- <v-col cols="12" lg="8">
      <TotalGrowth />
    </v-col> -->

  <!-- -------------------------------------------------------------------- -->
  <!-- Popular Stocks -->
  <!-- -------------------------------------------------------------------- -->
  <!-- <v-col cols="12" lg="4">
      <PopularStocks />
    </v-col>
  </v-row> -->
</template>

<style scoped>
.safety-banner {
  display: flex;
  justify-content: space-between;
  align-items: center;
  background-color: #f5f5f5;
  padding: 24px 32px;
  border-radius: 20px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.05);
  width: 100%;
}

.safety-text {
  font-size: 1.4rem;
  font-weight: bold;
  line-height: 1.8;
  color: #000;
}

.gongjaki {
  height: 140px;
  width: auto;
}
</style>
