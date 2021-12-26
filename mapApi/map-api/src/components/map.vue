<template>
  <div class="shorten">
    <form>
      <input type="text" placeholder="Shorten a link here..." v-model="url" />
      <div @click.prevent="postData" @click='response = !response' class="shorten_it_btn">Shorten it !</div>
    </form>
  </div>
  <div class="response" v-show='response'>
    <div class="long_link">{{url}}</div>
    <div v-for="(address, index) in addresses" :key="index">
      {{ address.full_short_link }}
    </div>
    <div class="copy" v-bind="copy"> Copy</div>
  </div>

</template>

<script>
import axios from "axios";
export default {
  name: "mapAdress",
  data() {
    return {
      addresses: [],
      url: "",
      response: false
    };
  },
  methods: {
    async postData() {
      await axios
        .get("https://api.shrtco.de/v2/shorten", {
          params: { url: this.url },
        })
        .then((response) => (this.addresses = response.data));
      console.log(this.addresses);
    },
  },
};
</script>

<style>
.shorten {
  width: 100%;
  margin-top: 50px;
  padding: 50px 0px;
  background: url("../assets/bg-shorten-desktop.svg") hsl(257, 27%, 26%);
  background-size: cover;
  border-radius: 10px;
}
.shorten form {
  display: flex;
  padding: 0 5%;
}
.shorten input {
  width: 80%;
  height: 50px;
  border-radius: 8px;
  border: none;
  padding-left: 20px;
}
.shorten_it_btn {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 15%;
  background: var(--primary);
  height: 50px;
  border-radius: 10px;
  margin-left: 5%;
  color: white;
  font-family: "Poppins";
  cursor: pointer;
}
/* ----- RESPONSE -----  */

.response {
  background: red;
  height: 50px;
}
</style>
