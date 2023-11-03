<template>
  <div class="home">
    
    <section class="frontpage">
      <Navbar/>
      <!-- <img src="../assets/background/leaf.png">
      <img src="../assets/background/leaf.png">
      <img src="../assets/background/leaf.png">
      <img src="../assets/background/leaf.png">
      <img src="../assets/background/leaf.png">
      <img src="../assets/background/leaf.png">
      <img src="../assets/background/leaf.png"> -->
      <div class="content">
        <small>Welcome to our</small>
        <h1>Plant Disease <br>Detection Website</h1>
      </div>
      <!-- <div class="image-container">
        <div class="card" :class="{ 'fade-up': fadeIn }" style="width: 18rem;">
          <div class="card-body">
            <h5 class="card-title">Introduction</h5>
            <p class="card-text">
              Global agriculture, contributing 4% to the GDP, faces challenges like pests and diseases affecting yields. 
              Traditional methods are slow, impacting profits. Modernizing with advanced technology like YOLOv5 and YOLOv8 improves disease detection, 
              aiding crop management decisions. This paper compares these models and introduces a valuable dataset for addressing agricultural challenges 
              and benchmarking progress.
            </p>
          </div>
        </div>
      </div> -->
      <div class="row justify-content-center">
        <div class="card-container" style="position: absolute; top: 100%; left: 50%; transform: translate(-50%, -50%); width: 50%;">
          <div class="card bg-white border-0 shadow form-card">
            <div class="card-body">
              <h1 class="text-dark text-center mb-5">Why to detect???</h1>
              <h5> <center>Please find this out below</center> </h5>
            </div>
          </div>
        </div>
      </div>
    </section>
    <br><br><br>
    <section class="lastpage">
      fjnwjfjnweibfhwebufwe8fbwefwe
    </section> 
  </div>
</template>

<script>
import Navbar from "../components/Navbar.vue"
export default {
  name: 'HomeView',
  components: {
    Navbar,
  },
  data() {
    return {
      fadeIn: false,
    };
  },
  mounted() {
    // Use a timeout to allow the image to load before fading in
    setTimeout(() => {
      this.fadeIn = true;
    }, 100);
  },
};
</script>

<style scoped>

.frontpage {
  width: 100%;
  height: 100vh;
  background-image: url('../assets/background/plant9.jpg');
  background-size: cover;
  background-position: center;
  position: relative; 
  overflow: hidden;
  z-index: 1000;  
  color: white;
}

/* .card { */
  /* position: absolute; */
  /* top: 150px; Adjust the top value as needed */
  /* right: 150px; Adjust the right value as needed */
  /* opacity: 0; */
  /* transform: translateY(20px); */
  /* transform: translate(20px,20px); */
  /* transition: opacity 0.5s ease, transform 0.5s ease; */
/* } */

/* .fade-up { */
  /* opacity: 1; */
  /* transform: translateY(0); */
  /* transform: translate(0,0); */
/* } */

.content {
  /* color: #fbfcfd;  #404464 #FF8D5C */
  color: #fbfcfd;
  position: absolute;
  top: 50%;
  left: 8%;
  transform: translateY(-50%);
}

h1 {
  font-size: 80px;
  line-height: 70px;
  margin: 10px 0 30px;
}
</style>

