<template>
  <div>
    <ul>
      <FriendNav text="HOME" />
      <FriendNav text="ABOUT US" />
      <FriendNav text="SERVICES" />
      <FriendNav text="HELP?" />
    </ul>
  </div>
  <section id="form">
    <FriendForm />
  </section>
</template>

<script>
import FriendNav from "./components/FriendNav.vue";
import FriendForm from "./components/FriendForm.vue";

export default {
  components: {
    FriendNav,
    FriendForm,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /* text-align: center; */
  color: #2c3e50;
  margin-top: 60px;
  width: 50%;
  margin: auto;
}
</style>
