<template>
  <div>
    <h1>Search iTunes</h1>
    <br>
    <v-layout>
      <v-flex md4 offset-md4>
        <v-form @submit.prevent="submit" ref="search" v-model="valid" lazy-validation>
          <v-text-field v-model="search" label="search" required autofocus></v-text-field>
        </v-form>
      </v-flex>
    </v-layout>
    <!-- <form @submit.prevent="submit">
      <input placeholder="Enter Artist Name" v-model="search" ref="search" autofocus>
    </form>-->
  </div>
</template>
<script>
export default {
  data() {
    return {
      search: ""
    };
  },
  methods: {
    submit(event) {
      this.$router.push(`results/${this.search}`);
    }
  }
};
</script>

<style scoped>
* {
  text-align: center;
}
h1 {
  padding: 20px;
}
</style>