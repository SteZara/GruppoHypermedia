<template>
  <!-- HERO CENTRALE CON IMMAGINE TONDA -->
  <div class="index-container">
    <div class="circle-menu-container">
      <section class="hero-section">
        <img src="/center/yoga_sunset.jpg" alt="Yoga meditazione" class="main-image" />

        <div class="icon-link top-left">
          <NuxtLink to="/about">
            <img src="/icons/about.png" alt="About Icon" />
            <span>About Us</span>
          </NuxtLink>
        </div>

        <div class="icon-link top-right">
          <NuxtLink to="/activities">
            <img src="/icons/courses.png" alt="Courses Icon" />
            <span>Courses</span>
          </NuxtLink>
        </div>

        <div class="icon-link bottom-left">
          <NuxtLink to="/teachers">
            <img src="/icons/instructors.png" alt="Instructors Icon" />
            <span>Instructors</span>
          </NuxtLink>
        </div>

        <div class="icon-link bottom-right">
          <NuxtLink to="/meditation">
            <img src="/icons/meditation.png" alt="Meditation Icon" />
            <span>Meditation</span>
          </NuxtLink>
        </div>
      </section>
    </div>
  </div>

  <!-- CARDS CENTRALI -->
  <section class="courses-section">
    <h2>Find out our courses proposals</h2>
    <div class="courses-cards">
      <div class="card">
        <img src="/cards/meditation_card.png" alt="Meditation" />
        <div class="card-label">Meditation Sessions<br />10:00 Saturday</div>
      </div>

      <div class="card">
        <img src="/cards/outdoor_card.png" alt="Outdoor Yoga" />
        <div class="card-label">Try Outdoor Yoga</div>
      </div>

      <div class="card">
        <img src="/cards/prenatal_card.png" alt="Prenatal Ashtanga" />
        <div class="card-label">Prenatal Ashtanga</div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
// nessuna logica per ora
</script>

<style scoped>
.index-container {
  z-index: 0;
}

.circle-menu-container {
  position: relative;
  height: 600px;
  background: url('/center/studio_background.jpg') no-repeat center center/cover;
  display: flex;
  justify-content: center;
  align-items: center;
}

/* SEZIONE HERO */
.hero-section {
  position: relative;
  height: 600px;
  display: flex;
  justify-content: center;
  align-items: center;
}

.main-image {
  width: 300px;
  height: 300px;
  border-radius: 50%;
  object-fit: cover;
  box-shadow: 0 0 20px rgba(0, 0, 0, 0.3);
  z-index: 1;
}

.icon-link {
  position: absolute;
  text-align: center;
  width: 120px;
  z-index: 2;
}

.icon-link img {
  width: 50px;
  height: 50px;
}

.icon-link span {
  display: block;
  font-size: 14px;
  font-weight: bold;
  margin-top: 5px;
}

/* POSIZIONAMENTO ICONE */
.top-left    { top: 20%;  left: 15%; }
.top-right   { top: 20%;  right: 15%; }
.bottom-left { bottom: 20%; left: 15%; }
.bottom-right{ bottom: 20%; right: 15%; }

/* SEZIONE CARD CORSI */
.courses-section {
  text-align: center;
  padding: 60px 20px;
  background: #f8f9fa;
}

.courses-section h2 {
  font-size: 24px;
  margin-bottom: 40px;
}

.courses-cards {
  display: flex;
  justify-content: center;
  gap: 30px;
  flex-wrap: wrap;
}

.card {
  width: 250px;
  position: relative;
  overflow: hidden;
  border-radius: 20px;
}

.card img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  border-radius: 20px;
}

.card-label {
  position: absolute;
  color: white;
  font-size: 18px;
  font-weight: 500;
  bottom: 20px;
  left: 20px;
  text-shadow: 1px 1px 4px black;
}
</style>