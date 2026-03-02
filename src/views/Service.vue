<template>
  <section class="service-section service-animate" ref="serviceSection">
    <h2 class="service-title">What We Offer</h2>
    <p class="service-desc">
      Cleaning is a tough challenge for everyone. But we’re always up for any challenge!<br>
      Our expert team has the perfect solution for every cleaning need, ensuring your home stays spotless and fresh.
    </p>
    <h3 class="service-highlight">Aircon Cleaning</h3>
    <div class="aircon-cards">
      <div class="aircon-card">
        <img src="https://images.unsplash.com/photo-1506744038136-46273834b3fb?auto=format&fit=crop&w=400&q=80" alt="Window Type" />
        <div class="card-overlay">
          <div class="card-title">Window<br>Type</div>
          <div class="card-price">P920</div>
        </div>
      </div>
      <div class="aircon-card">
        <img src="https://images.unsplash.com/photo-1506744038136-46273834b3fb?auto=format&fit=crop&w=400&q=80" alt="Split Type" />
        <div class="card-overlay">
          <div class="card-title">Split<br>Type</div>
          <div class="card-price">P1,530</div>
        </div>
      </div>
      <div class="aircon-card">
        <img src="https://images.unsplash.com/photo-1519125323398-675f0ddb6308?auto=format&fit=crop&w=400&q=80" alt="Floor Mounted" />
        <div class="card-overlay">
          <div class="card-title">Floor<br>Mounted</div>
          <div class="card-price">P2,960</div>
        </div>
      </div>
      <div class="aircon-card">
        <img src="https://images.unsplash.com/photo-1519125323398-675f0ddb6308?auto=format&fit=crop&w=400&q=80" alt="Casette Type" />
        <div class="card-overlay">
          <div class="card-title">Casette<br>Type</div>
          <div class="card-price">P5,490</div>
        </div>
      </div>
    </div>
    <div class="aircon-book-section">
      <button class="aircon-book-btn">BOOK NOW</button>
      <div class="aircon-hotline">
        Or Call our Aircon Cleaning Hotline<br>
        <span class="aircon-hotline-number">(0931)-728-8845</span>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'ServiceSection',
  mounted() {
    const section = this.$refs.serviceSection;
    if (!section) return;
    const observer = new window.IntersectionObserver((entries) => {
      entries.forEach(entry => {
        if (entry.isIntersecting) {
          section.classList.add('service-animate-active');
        } else {
          section.classList.remove('service-animate-active');
        }
      });
    }, { threshold: 0.2 });
    observer.observe(section);
  }
}
</script>

<style scoped>
.service-section {
  text-align: center;
  margin: 100px auto 0 auto;
  max-width: 1200px;
  padding: 0 16px;
}
.service-title {
  font-size: 3rem;
  color: #4a90e2;
  /* font-weight: 700; */
  margin-bottom: 30px;
}
.service-desc {
  font-size: 1.8rem;
  color: #3b7fc4;
  margin-bottom: 40px;
  line-height: 1.3;
}
.service-highlight {
  font-size: 3rem;
  color: #4a90e2;
  font-weight: 700;
  margin-bottom: 30px;
}
.aircon-cards {
  display: flex;
  justify-content: center;
  gap: 24px;
  margin: 48px 0 0 0;
}
.aircon-card {
  position: relative;
  width: 350px;
  height: 350px;
  border-radius: 8px;
  overflow: hidden;
  box-shadow: 0 4px 24px rgba(0,0,0,0.08);
}
.aircon-card img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  filter: brightness(0.7);
}
.card-overlay {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  color: #fff;
  font-weight: 700;
}
.card-title {
  font-size: 2.4rem;
  text-align: center;
  margin-bottom: 24px;
  text-shadow: 0 2px 8px rgba(0,0,0,0.18);
}
.card-price {
  font-size: 3.2rem;
  color: #ffe12b;
  font-weight: 700;
  text-shadow: 0 2px 8px rgba(0,0,0,0.18);
}
.aircon-book-section {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin: 48px 0 0 0;
}
.aircon-book-btn {
  background: #ffe12b;
  color: #2196f3;
  font-weight: 700;
  font-size: 2rem;
  border: none;
  border-radius: 10px;
  padding: 20px 60px;
  cursor: pointer;
  margin-bottom: 24px;
  transition: background 0.2s;
}
.aircon-book-btn:hover {
  background: #fff200;
}
.aircon-hotline {
  color: #3b7fc4;
  font-size: 1.6rem;
  text-align: center;
}
.aircon-hotline-number {
  color: #2196f3;
  font-size: 2.6rem;
  font-weight: 700;
  display: block;
  margin-top: 8px;
  margin-bottom: 8px;
}
.aircon-img-animate {
  opacity: 1;
  animation: airconScaleAnim 1.2s cubic-bezier(0.23, 1, 0.32, 1);
}

@keyframes airconScaleAnim {
  0% {
    transform: scale(0.85);
  }
  50% {
    transform: scale(1.15);
  }
  100% {
    transform: scale(0.85);
  }
}
/* Vue transition for ServiceSection */
.fade-slide-enter-active, .fade-slide-leave-active {
  transition: opacity 2s cubic-bezier(0.23, 1, 0.32, 1), transform 2s cubic-bezier(0.23, 1, 0.32, 1);
}
.fade-slide-enter, .fade-slide-leave-to {
  opacity: 0;
  transform: translateY(40px);
}
.service-animate {
  opacity: 0;
  transform: translateY(40px);
  transition: opacity 1.2s cubic-bezier(0.23, 1, 0.32, 1), transform 1.2s cubic-bezier(0.23, 1, 0.32, 1);
}
.service-animate-active {
  opacity: 1;
  transform: none;
}
/* Fade-in animation for ServiceSection */
</style>


