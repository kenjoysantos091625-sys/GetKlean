
<template>
  <div class="fade-in">
    <div class="aircon-hero">
      <div class="hero-left">
        <h1>Aircon Cleaning</h1>
        <p class="subtitle">Fresh air, cool life!<br>Keep your home cool and relaxing.</p>
        <div class="hero-actions">
          <button class="book-btn">BOOK NOW</button>
          <div class="hotline">
            <span class="hotline-icon">📞</span>
            <div>
              <span class="hotline-label">Call our hotline</span><br>
              <span class="hotline-number">(0919)056-8415</span>
            </div>
          </div>
        </div>
      </div>
      <div class="hero-right">
        <img class="hero-img" src="@/assets/cleaningaircon.png" alt="Aircon Cleaning" />
      </div>
    </div>
    <ServiceSection id="services-section"/>
    <TestimonialView />
  </div>
</template>


<script>
import ServiceSection from './Service.vue';
import TestimonialView from './Testimonial.vue';
export default {
  name: 'HomeView',
  components: {
    ServiceSection,
    TestimonialView
  }
}
</script>

<style scoped>
.fade-in {
  opacity: 0;
  transform: translateY(40px);
  animation: fadeInUp 1.2s cubic-bezier(0.23, 1, 0.32, 1) forwards;
}

@keyframes fadeInUp {
  to {
    opacity: 1;
    transform: none;
  }
}
.aircon-hero {
  display: flex;
  min-height: 90vh;
  background: #f7f6f6;
}
.hero-left {
  flex: 1;
  display: flex;
  flex-direction: column;
  justify-content: center;
  padding: 60px 40px 60px 60px;
}
.hero-left h1 {
  font-size: 6rem;
  color: #4a90e2;
  font-weight: 700;
  margin-bottom: 24px;
}
.subtitle {
  font-size: 3rem;
  color: #4a90e2;
  margin-bottom: 36px;
}
.hero-actions {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 24px;
  margin-bottom: 40px;
}
.book-btn {
  background: #ffe12b;
  color: #2196f3;
  font-weight: 600;
  font-size: 2.2rem;
  border: none;
  border-radius: 10px;
  padding: 20px 40px;
  cursor: pointer;
  transition: background 0.2s;
}
.book-btn:hover {
  background: #fff200;
}
.hotline {
  display: flex;
  align-items: center;
  gap: 12px;
  font-size: 1.8rem;
}
.hotline-icon {
  font-size: 2.2rem;
  color: #4a90e2;
  border: 2px solid #4a90e2;
  border-radius: 50%;
  padding: 8px;
  margin-right: 4px;
}
.hotline-label {
  color: #4a90e2;
  font-size: 1.6rem;
}
.hotline-number {
  color: #4a90e2;
  font-size: 2.4rem;
  font-weight: bold;
}
.hero-progress {
  display: flex;
  align-items: center;
  margin-top: 40px;
}
.progress-num {
  color: #4a90e2;
  font-size: 3rem;
  font-weight: 600;
  margin-right: 16px;
}
.progress-bar {
  flex: 1;
  height: 6px;
  background: #ffe12b;
  border-radius: 3px;
}
.hero-right {
  flex: 1;
  display: flex;
  align-items: center;
  justify-content: center;
  background: #fff;
  border-radius: 0 0 0 60px;
  overflow: hidden;
  height: 100%;
  min-height: 80vh;
  max-width: 50vw;
  box-sizing: border-box;
}
.hero-img {
  display: block;
  margin: auto;
  width: 100%;
  max-width: 900px;
  height: 2000px;
  max-height: 100vh;
  height: auto;
  object-fit: contain;
  border-radius: 0 0 0 60px;
  box-shadow: 0 4px 24px rgba(0,0,0,0.08);
}
</style>
