<script >
export default {
  data() {
    return {
      fname: "",
      lname: "",
      email: "",
    };
  },
  methods: {
    submitForm() {
      // Handle form submission here
      console.log(
        "Form submitted with name:",
        this.name,
        "and email:",
        this.email
      );

      // Reset form fields
      this.fname = "";
      this.lname = "";
      this.email = "";
    },
  },
};
</script>

<template>
  <div>
    <h1>ordering form</h1>
    <form v-on:submit.prevent="submitForm">
      <p>
        First Name
        <input type="text" required placeholder="bini" v-model="fname" />
      </p>
      <p>
        Last Name
        <input type="text" placeholder="getachew" v-model="lname" />
      </p>
      <p>
        Email
        <input type="email" placeholder="getachew" v-model="email" />
      </p>
      <p>
        Type of artwork
        <input type="number" placeholder="glass" />
      </p>
      <p>
        Artist Name
        <input type="number" placeholder="honelign" />
      </p>
      <p>
        Delivery date
        <input type="date" placeholder="getachew" />
      </p>
      <p>
        Price of Artwork
        <input type="number" placeholder="$" />
      </p>

      <button type="submit">submit</button>
    </form>
  </div>
</template>

<style scoped>
form {
  position: relative;
  display: flex;
  flex-direction: column;
  max-width: 500px;
  margin: auto;
  background: linear-gradient(to bottom, #ffffff, #f2f2f2);
  transition: background 0.5s ease-in-out;
}
button[type="submit"] {
  background-color: rgb(86, 76, 175); /* Green */
  border: none;
  color: white;
  padding: 10px 20px;
  text-align: center;
  text-decoration: none;
  display: inline-block;
  font-size: 16px;
  margin-top: 1rem;
}
p {
  font-size: 1.2rem;
  margin-bottom: 0.5rem;
  margin-left: 2rem;
}
input {
  padding: 0.5rem;
  border-radius: 0.5rem;
  border: none;
  box-shadow: rgba(0, 0, 0, 0.2) 0px 1px 2px;
  position: absolute;
  right: 100px;
}
input[type="submit"]:hover {
  background-color: #3e8e41; /* Dark green */
}
form:hover {
  background: linear-gradient(to bottom, #f2f2f2, #ffffff);
}
</style>