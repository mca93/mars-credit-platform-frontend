<template>
  <div class="page-table column scrollable only-y" :class="{'flex':!isMobile, 'overflow':isMobile}">
    <div class="page-header">
      <h1>Manage White List</h1>
      <h4>A client can be removed from the list if he choose to.</h4>

      <SearchClient class="padding"></SearchClient>
      <DisplayClient></DisplayClient>
    </div>
  </div>
</template>

<script>
import SearchClient from "../../components/Front-client/SearchClient.vue";
import DisplayClient from "../../components/Front-client/DisplayClient.vue";

export default {
  props: [""],
  data() {
    return {};
  },
  components: {
    SearchClient,
    DisplayClient
  }
};
</script>

<style>
.padding {
  padding-top: 10px;
}
.page-header h4 {
  padding-top: 3px;
  margin-top: 1px;
  padding-bottom: 5px;
}
</style>