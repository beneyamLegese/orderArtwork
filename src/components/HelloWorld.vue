<script setup>
import { ref } from "vue";

const count = ref(0);
</script>

<template>
<div>
  <h1>ordering form</h1>
 <form v-on:submit.prevent="addItem">
    <p>
      First Name
      <input type="text" required placeholder="bini" >
    </p>
    <p>
      Last Name
      <input type="number" placeholder="getachew">
    </p>
     <p>
      type of artwork
      <input type="number" placeholder="glass">
    </p>
     <p>
      Artist Name
      <input type="number" placeholder="honelign">
       <p>
      delivery date
      <input type="date" placeholder="getachew">
    </p>
     <p>
      Price of Artwork
      <input type="number" placeholder="$" >
    </p>
    </p>
    <button type="submit">submit</button>
  </form>
  </div>
</template>

<style scoped>
button {
  font-weight: bold;
}
</style>