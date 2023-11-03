<!-- <template>
  <div class="nav">
    <nav class="navbar navbar-expand-sm navbar-light">
    <div class="container">
      <router-link class="navbar-brand text-style white-text" :to="{name: 'Dashboard'}">Plant Disease Detection</router-link>
      <div class="collapse navbar-collapse" id="navbarNav">
        <ul class="navbar-nav ms-auto">

          <li class="nav-item">
            <router-link class="btn button" :to="{name: 'Home'}">Home</router-link>
          </li>
          
          <li class="nav-item">
            <router-link class="btn button" :to="{name: 'Dashboard'}">Dashboard</router-link>
          </li>

          <li class="nav-item">
            <router-link class="btn button" :to="{name: 'AboutUs'}">About Us</router-link>
          </li>

          <li class="nav-item">
            <router-link class="btn button" :to="{name: 'ProjectDetails'}">Project Details</router-link>
          </li>
          
          
        </ul>
      </div>
    </div>
    </nav>
  </div>
</template>

<script>
export default {

}
</script>

<style>
.nav {
  width: 85%;
  margin: auto;
  display: flex;
  align-items: center;
  justify-content: space-between;
  /* color: transparent; */
}

.nav .button {
  color: #fbfcfd;
  padding: 10px 25px;
  background: transparent;
  border: 1px solid #fff;
  border-radius: 20px;
  outline: none;
  margin-right: 10px;
}

.white-text {
  color: white;
}

</style> -->

<template>
  <div class="nav">
    <nav class="navbar navbar-expand-sm navbar-light">
      <div class="container">
        <router-link class="navbar-brand text-style white-text" :to="{name: 'Dashboard'}">Plant Disease Detection</router-link>
        <div class="collapse navbar-collapse" id="navbarNav">
          <ul class="navbar-nav ms-auto">
            <li class="nav-item">
              <router-link class="btn button" :to="{name: 'Home'}">Home</router-link>
            </li>
            <li class="nav-item">
              <router-link class="btn button" :to="{name: 'Dashboard'}">Dashboard</router-link>
            </li>
            <li class="nav-item">
              <router-link class="btn button" :to="{name: 'AboutUs'}">About Us</router-link>
            </li>
            <li class="nav-item">
              <router-link class="btn button" :to="{name: 'ProjectDetails'}">Project Details</router-link>
            </li>
          </ul>
        </div>
      </div>
    </nav>
  </div>
</template>

<style>
.nav {
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
}

.navbar {
  width: 85%;
}

.nav .button {
  color: #fbfcfd;
  padding: 10px 25px;
  background: transparent;
  border: 1px solid #fff;
  border-radius: 20px;
  outline: none;
  margin-right: 10px;
}

.white-text {
  color: white;
}
</style>
