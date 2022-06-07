<template>
  <ag-grid-vue
    style="width: 600px; height: 450px"
    class="ag-theme-alpine"
    :columnDefs="columnDefs"
    :rowData="rowData"
    enableSorting:true
  >
  </ag-grid-vue>
</template>

<script>
import "ag-grid-community/dist/styles/ag-grid.css";
import "ag-grid-community/dist/styles/ag-theme-alpine.css";
import { AgGridVue } from "ag-grid-vue3";

export default {
  name: "App",
  components: {
    AgGridVue,
  },
  setup() {
    return {
      columnDefs: [
        { headerName: "Flight", field: "flight", filter: true},
        { headerName: "Departure", field: "departure", filter: true },
        { headerName: "Destination", field: "destination", filter: true},
      ],
      rowData: [
        { flight: "Flight 1", departure: "Celica", destination: "Rome" },
        { flight: "Flight 2", departure: "Mondeo", destination: "Virginia" },
        { flight: "Flight 3", departure: "Boxster", destination: "Key West" },
        { flight: "Flight 4", departure: "Celica", destination: "Rome" },
        { flight: "Flight 5", departure: "Mondeo", destination: "Virginia" },
        { flight: "Flight 6", departure: "Boxster", destination: "Key West" },
        { flight: "Flight 7", departure: "Celica", destination: "Rome" },
        { flight: "Flight 8", departure: "Mondeo", destination: "Virginia" },
        { flight: "Flight 9", departure: "Boxster", destination: "Key West" },
      ],
    };
  },
};
</script>