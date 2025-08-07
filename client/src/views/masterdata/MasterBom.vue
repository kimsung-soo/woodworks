<template>
  <!-- The AG Grid component -->
  <ag-grid-vue :rowSelection="rowSelection" :rowData="rowData" :columnDefs="colDefs" style="width: 900px; height: 500px"> </ag-grid-vue>
</template>

<script>
import { ref } from 'vue';
import { AgGridVue } from 'ag-grid-vue3'; // Vue Data Grid Component
import { AllCommunityModule, ModuleRegistry } from 'ag-grid-community';
ModuleRegistry.registerModules([AllCommunityModule]);
export default {
  name: 'App',
  components: {
    AgGridVue // Add Vue Data Grid component
  },
  setup() {
    const rowSelection = {
      mode: 'multiRow'
    };
    // Row Data: The data to be displayed.
    const rowData = ref([
      { make: 'Tesla', model: 'Model Y', price: 64950, electric: true },
      { make: 'Ford', model: 'F-Series', price: 33850, electric: false },
      { make: 'Toyota', model: 'Corolla', price: 29600, electric: false }
    ]);

    // Column Definitions: Defines the columns to be displayed.
    const colDefs = ref([
      { field: 'make' },
      { field: 'model' },
      { field: 'price' },
      {
        field: 'electric',
        headerName: 'Electric',
        editable: true,
        cellRenderer: 'agCheckboxCellRenderer',
        cellEditor: 'agCheckboxCellEditor'
      }
    ]);

    return {
      rowData,
      colDefs,
      rowSelection
    };
  }
};
</script>
