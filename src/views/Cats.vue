<template>
  <div>
    <h1>Cats for adoption</h1>
    <b-table striped hover :items="cats" :outlined="true">
      <template v-slot:cell(name)="data">
        <router-link :to="`/pet/cats/${data.index}`">{{data.value}}</router-link>
      </template>
    </b-table>
  </div>
</template>

<script>
import { mapState } from "vuex";

export default {
  data() {
    return {};
  },
  computed: {
    ...mapState(["cats"]),
  },
};
</script>
