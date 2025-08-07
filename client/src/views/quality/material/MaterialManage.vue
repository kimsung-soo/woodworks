<script setup lang="ts">
import { ref, shallowRef } from 'vue';

import BaseBreadcrumb from '@/components/shared/BaseBreadcrumb.vue';

const page = ref({ title: '원자재검수 관리' });
const breadcrumbs = shallowRef([
  {
    title: 'Others',
    disabled: false,
    href: '#'
  },
  {
    title: 'Sample Page',
    disabled: true,
    href: '#'
  }
]);
</script>

<template>
  <BaseBreadcrumb :title="page.title" :breadcrumbs="breadcrumbs"></BaseBreadcrumb>
  <v-row>
    <v-col cols="12" md="12">
      <table class="table table-hover">
        <thead>
          <tr>
            <th scope="col">기준명</th>
            <th scope="col">허용수치</th>
            <th scope="col">판정</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th scope="row">함수율</th>
            <td>Mark</td>
            <td><radio>● 합격</radio></td>
          </tr>
          <tr>
            <th scope="row">외관결점</th>
            <td>Jacob</td>
            <td>Thornton</td>
          </tr>
          <tr>
            <th scope="row">치수정밀도</th>
            <td colspan="2">Larry the Bird</td>
          </tr>
          <tr>
            <th scope="row">강도</th>
            <td colspan="2">Larry the Bird</td>
          </tr>
          <tr>
            <th scope="row">외관/표면 결함</th>
            <td colspan="2">Larry the Bird</td>
          </tr>
        </tbody>
      </table>
    </v-col>
  </v-row>
</template>
