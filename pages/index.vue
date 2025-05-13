<template>
  <div class="index-container">
    <div class="main-image">
      <img src="/center/yoga_sunset.jpg" alt="Yoga meditazione" />
    </div>

    <div class="icon-link top-left">
      <NuxtLink to="/about">
        <img src="/icons/about.png" alt="About Icon" />
        <span>about us</span>
      </NuxtLink>
    </div>

    <div class="icon-link top-right">
      <NuxtLink to="/careers">
        <img src="/icons/career.png" alt="Careers Icon" />
        <span>careers</span>
      </NuxtLink>
    </div>

    <div class="icon-link bottom-left">
      <NuxtLink to="/teachers">
        <img src="/icons/teachers.png" alt="Teachers Icon" />
        <span>instructors</span>
      </NuxtLink>
    </div>

    <div class="icon-link bottom-right">
      <NuxtLink to="/activities">
        <img src="/icons/activity.png" alt="Activity Icon" />
        <span>activity</span>
      </NuxtLink>
    </div>
  </div>
</template>

<script setup lang="ts">
// nessuna logica per ora
</script>

<style scoped>
.index-container {
  position: relative;
  height: calc(100vh - 160px);
  display: flex;
  justify-content: center;
  align-items: center;
}

.main-image img {
  width: 300px;
  height: 300px;
  border-radius: 50%;
  object-fit: cover;
  box-shadow: 0 0 15px rgba(0, 0, 0, 0.2);
}

.icon-link {
  position: absolute;
  text-align: center;
  width: 120px;
}

.icon-link img {
  width: 40px;
  height: 40px;
  margin-bottom: 5px;
}

.icon-link span {
  display: block;
  font-size: 14px;
  color: #333;
  font-weight: 600;
}

.top-left {
  top: 15%;
  left: 22%;
}

.top-right {
  top: 15%;
  right: 22%;
}

.bottom-left {
  bottom: 15%;
  left: 22%;
}

.bottom-right {
  bottom: 15%;
  right: 22%;
}
</style>