<template>
  <div class="details">
    <Navbar />
    <div class="container">
      <div class="row mt-4">
        <div class="col-sm-4 text-center">
          <h3>Research Paper</h3>
        </div>
        <div class="col-sm-8">
          <p><strong>Plant Diesase Detection</strong></p>
          <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>
        </div>
      </div>
      <div class="row mt-4">
        <div class="col-sm-4 text-center">
          <h3>App</h3>
        </div>
        <div class="col-sm-8">
          <p><strong>Yolo v8 and web dev</strong></p>
          <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>
        </div>
      </div>
    </div>   
  </div>
</template>

<script>
import Navbar from "../components/Navbar.vue"
export default {
  name: "ProjectDetails",
  components: {
    Navbar,
  },
}
</script>

<style scoped>

body{
  margin: 0;
  padding: 0;
  
}

.details {
  /* color: #d8f3dc; */
  color: #7A7800;
}

</style>