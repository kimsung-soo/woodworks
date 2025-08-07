<template>
  <div class="container">
    <form @submit.prevent>
      <label for="code">설비 코드</label>
      <input type="text" id="code" v-model="equipment.code" required />

      <label for="name">설비명</label>
      <input type="text" id="name" v-model="equipment.name" required />

      <label for="type">설비유형</label>
      <input type="text" id="type" v-model="equipment.type" />

      <label>사용유무</label>
      <div>
        <label><input type="radio" value="사용" v-model="equipment.useYn" /> 사용</label>
        <label><input type="radio" value="미사용" v-model="equipment.useYn" /> 미사용</label>
      </div>

      <label for="maker">제조사</label>
      <input type="text" id="maker" v-model="equipment.maker" />

      <label for="makeDate">설비 제조일</label>
      <input type="date" id="makeDate" v-model="equipment.makeDate" />

      <label for="installDate">설비 설치일</label>
      <input type="date" id="installDate" v-model="equipment.installDate" />

      <label for="checkCycle">점검 주기(일)</label>
      <input type="number" id="checkCycle" v-model="equipment.checkCycle" />

      <label for="manager">담당자</label>
      <input type="text" id="manager" v-model="equipment.manager" required />

      <button type="button" class="btn btn-primary">등록</button>
    </form>
  </div>
</template>

<script setup>
import axios from 'axios';
import { reactive } from 'vue';

const equipment = reactive({
  code: '',
  name: '',
  type: '',
  useYn: '사용',
  maker: '',
  makeDate: '',
  installDate: '',
  checkCycle: '',
  manager: ''
});
</script>

<style scoped>
/* Style inputs with type="text", select elements and textareas */
input[type='text'],
select,
textarea {
  width: 100%; /* Full width */
  padding: 12px; /* Some padding */
  border: 1px solid #ccc; /* Gray border */
  border-radius: 4px; /* Rounded borders */
  box-sizing: border-box; /* Make sure that padding and width stays in place */
  margin-top: 6px; /* Add a top margin */
  margin-bottom: 16px; /* Bottom margin */
  resize: vertical; /* Allow the user to vertically resize the textarea (not horizontally) */
}

/* Style the submit button with a specific background color etc */

/* Add a background color and some padding around the form */
.container {
  border-radius: 5px;
  background-color: #f2f2f2;
  padding: 20px;
}
</style>
