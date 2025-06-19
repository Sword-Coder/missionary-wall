<!--<template>
  <q-page class="flex flex-center">
    <img
      alt="Quasar logo"
      src="~assets/MissionaryBackground.png"
      style="width: 100%; height: 100vh"
    />

    <div
      class="absolute text-white text-center"
      style="background-color: red; top: 50%; left: 50%; transform: translate(-50%, -50%)"
    >
      <h1 class="text-h2">Today's Missionary Updates</h1>
      <p class="text-subtitle1">Your journey starts here</p>
      <q-btn
        class="q-mt-md"
        color="primary"
        label="Get Started"
        to="/missionaries"
        style="width: 200px; height: 50px; font-size: 18px"
      />
    </div>
  </q-page>
</template>

<script setup></script>
-->
<template>
  <q-page class="missionary-layout">
    <div class="content-overlay"></div>

    <!-- Updates Section (Top Left) -->
    <div class="updates-container">
      <div class="title text-h6">Today's Updates</div>
      <div class="update-item">1. Visited local village school</div>
      <div class="update-item">2. Held Bible study with 15 attendees</div>
      <div class="update-item">3. Medical outreach scheduled</div>
      <div class="update-item">4. New contacts made in community</div>
    </div>

    <!-- Prayer Requests (Top Right) -->
    <div class="prayer-container">
      <div class="title text-h6">Prayer Requests</div>
      <div class="prayer-item">1. Health for team members</div>
      <div class="prayer-item">2. Open hearts in village</div>
      <div class="prayer-item">3. Funding for new project</div>
      <div class="prayer-item">4. Safety in travels</div>
    </div>

    <!-- Mission Field (Bottom Left) -->
    <div class="country-container">
      <div class="title text-h6">Current Mission Field</div>
      <div class="country-name">Kenya</div>
      <div>Serving since: January 2020</div>
    </div>

    <!-- Floating Family Photo (Bottom Right) -->
    <img alt="Missionary family" src="~assets/Tonog.png" class="family-photo" />
    <!-- Main CTA Button (Center) -->
    <!--
    <div class="absolute-center text-center" style="z-index: 5">
      <h1 class="text-h2 text-white">Today's Missionary Updates</h1>
      <p class="text-subtitle1 text-white q-mb-md">Your journey starts here</p>
      <q-btn
        color="primary"
        label="Get Started"
        to="/missionaries"
        style="width: 200px; height: 50px; font-size: 18px"
      />
    </div>
    -->
  </q-page>
</template>

<script>
export default {
  name: 'MissionaryUpdates',
}
</script>

<style scoped>
.missionary-layout {
  position: relative;
  height: 100vh;
  background: url('~assets/MissionaryBackground.png') no-repeat center center;
  background-size: cover;
}
.content-overlay {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.2);
}
.updates-container,
.prayer-container {
  width: 600px;
  height: 500px;
  position: absolute;
  background: rgba(255, 255, 255, 0.9);
  border-radius: 10px;
  padding: 15px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
}
.updates-container {
  top: 20px;
  left: 20px;
}
.prayer-container {
  top: 20px;
  right: 20px;
}
.country-container {
  position: absolute;
  width: 600px;
  bottom: 20px;
  left: 20px;
  background: rgba(255, 255, 255, 0.9);
  border-radius: 10px;
  padding: 15px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
}
.family-photo {
  position: absolute;
  bottom: 20px;
  right: 50px;
  width: 300px;
  height: 300px;
  border-radius: 50%;
  border: 5px solid white;
  box-shadow: 0 10px 20px rgba(0, 0, 0, 0.3);
  transition: all 0.3s ease;
}
.family-photo:hover {
  transform: scale(1.05);
  box-shadow: 0 15px 25px rgba(0, 0, 0, 0.4);
}
.title {
  font-weight: bold;
  margin-bottom: 10px;
  text-shadow:
    #000 0px 0px 1px,
    #000 0px 0px 1px,
    #000 0px 0px 1px,
    #000 0px 0px 1px,
    #000 0px 0px 1px,
    #000 0px 0px 1px;
  color: #f8d544;
}
.update-item,
.prayer-item {
  padding: 8px 0;
  border-bottom: 1px solid #eee;
}
.update-item:last-child,
.prayer-item:last-child {
  border-bottom: none;
}
.country-name {
  font-size: 3.5rem;
  font-weight: bold;
  text-shadow:
    #000 0px 0px 6px,
    #000 0px 0px 6px,
    #000 0px 0px 6px,
    #000 0px 0px 6px,
    #000 0px 0px 6px,
    #000 0px 0px 6px;
  color: #f8d544;
}
@media (max-width: 1023px) {
  .updates-container,
  .prayer-container {
    width: 250px;
  }
}
@media (max-width: 767px) {
  .updates-container,
  .prayer-container {
    width: 200px;
    padding: 10px;
  }
  .family-photo {
    width: 150px;
    height: 150px;
  }
}
</style>
