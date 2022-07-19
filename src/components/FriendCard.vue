<template>
  <div class="card-group">
    <div class="card" v-for="value in dataCard" :key="value">
      <div>
        <h1>{{ value.firstName }} {{ value.lastName }}</h1>
        <P>{{ value.comments }}</P>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  props: {
    dataCard: [],
  },
  
};
</script>

<style>
.card {
  width: 80%;
  padding: 15px;
  margin: auto;
  box-shadow: rgba(99, 99, 99, 0.2) 0px 2px 8px 0px;
}
.card-group {
  margin-top: 25px;
}

</style>
