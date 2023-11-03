<template>
  <div class="about">
    <Navbar />
    <br><h2>About Us</h2><br><br>
    <div class="container">
      <div v-for="(name, index) in Names" :key="index" class="row mt-2">
        <div class="col-md-4">
          <img src="https://cdn.pixabay.com/photo/2015/04/23/22/00/tree-736885_1280.jpg" width="250" height="250">
        </div>
        <div class="col-md-8 info-container">
          <div class="info">
            <h4>{{ name }}</h4>
            <p>{{ Descrtiption[index] }}</p>
            <p> <b>Contributions:</b> {{ Contribution[index] }}</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Navbar from "../components/Navbar.vue"
export default {
  name: "AboutUs",
  components: {
    Navbar,
  },
  data() {
    return {
      Names: ["Mihir Mengde", "Rishabh Jain", "Vaibhav Hawaldar"],
      Descrtiption: [
        "MM is a coder. Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.",
        "RJ is a coder. Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.",
        "VH is a coder. Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua."
      ],
      Contribution: [
        "1,2,3",
        "1,2,3",
        "1,2,3"
      ]
    };
  }
}
</script>

<style scoped>
h2 {
  text-align: center;
  color:#d8f3dc;
}

img{
  border-radius: 50%;
}
.info-container {
  display: flex;
  align-items: center;
}
.info {
  padding: 20px;
  border: 1px solid #ccc;
}

body {
  background-color: #d8f3dc;  /* Light green background */
  color: #2a9d8f;            /* Dark green text color */
}
</style>