<template>
  <div class="form-input">
    <form action="" @submit.prevent="onAdd">
      <div>
        <input
          class="width"
          type="text"
          placeholder="First Name"
          v-model="firstName"
        />
      </div>
      <div>
        <input
          class="width"
          type="text"
          placeholder="Last Name"
          v-model="lastName"
        />
      </div>
      <div>
        <input
          class="width"
          type="text"
          placeholder="Comments"
          v-model="comments"
        />
      </div>
      <div>
        <button class="width">ADD</button>
      </div>
    </form>
  </div>
  <div >
    <Card :dataCard="dataUser" />
  </div>
</template>

<script>
import Card from "./FriendCard.vue";
export default {
  data() {
    return {
      firstName: "",
      lastName: "",
      comments: "",
      dataUser: [],
    };
  },
  methods: {
    onAdd() {
      let dataObject = {};
      dataObject.firstName = this.firstName;
      dataObject.lastName = this.lastName;
      dataObject.comments = this.comments;
      if (this.firstName != "" && this.lastName != "" && this.comments != "") {
        this.dataUser.push(dataObject);
        this.firstName = "";
        this.lastName = "";
        this.comments = "";
      }
    },
  },
  components: {
    Card,
  },
};
</script>

<style>
.form-input {
  margin-top: 15px;
}
form {
  box-shadow: rgba(0, 0, 0, 0.24) 0px 3px 8px;
  width: 80%;
  margin: auto;
  padding: 15px;
   text-align: center;
}
.width {
  margin-top: 10px;
  padding: 10px;
  width: 80%;
}
button {
  background: rgb(171, 170, 170);
  color: white;
  border: none;
  font-weight: bold;
}
</style>
