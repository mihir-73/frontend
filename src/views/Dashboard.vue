<template>
    <div class="dashboard">
      <Navbar />
      <h2>Dashboard</h2>
      <div class="content mt-5">Please click on the crop which you need detection with. And then upload your image on the next page</div>
      <div class="container mt-5">
        <div class="row">
          <div v-for="(crop, index) in crops" :key="index" class="col-sm-4">
            <router-link :to="{ name: 'Crop', params: { crop_name: crop.name } }">
                <div class="crop-box" @mouseover="showCropName(index)" @mouseout="hideCropName(index)">
                  <img :src="crop.image" alt="Crop Image" class="img-fluid">
                  <div class="crop-info">
                    <h5 v-show="hoveredCropIndex === index">{{ crop.name }}</h5>
                  </div>
                </div>
            </router-link>
          </div>
        </div>
      </div>
    </div>
</template>

<script>
import Navbar from "../components/Navbar.vue"
export default {
  name: "Dashboard",
  components: {
    Navbar,
  },
  data() {
    return {
    crops: [
      { name: "Wheat", image: require("@/assets/crops/wheat.jpg") },
      { name: "Chili", image: require("@/assets/crops/chili.jpg") },
      { name: "Bhindi", image: require("@/assets/crops/bhindi.jpg") },
      { name: "Corn", image: require("@/assets/crops/corn.jpg") },
      // Add more crops as needed
    ],
    hoveredCropIndex: null,
    };
  },
  methods: {
    showCropName(index) {
      this.hoveredCropIndex = index;
    },
    hideCropName() {
      this.hoveredCropIndex = null;
    },
  }
}
</script>

<style scoped>



.crop-box {
  position: relative;
  overflow: hidden;
  margin-bottom: 20px;
}

.crop-box img {
  transition: transform 0.3s ease;
  max-width: 100%;
  max-height: 100%;
}

.crop-info {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  background: rgba(0, 0, 0, 0.7);
  color: #fff;
  opacity: 0;
  transition: opacity 0.3s ease;
}

.crop-info h5 {
  margin: 0;
}

.crop-box:hover img {
  transform: scale(1.1);
}

.crop-box:hover .crop-info {
  opacity: 1;
}

img {
  height: 200px;
  width: 450px;
}

body {
  background-color: #d8f3dc;  /* Light green background */
  color: #2a9d8f;            /* Dark green text color */
  
}


</style>