<template>
  <div id="app">
    <div class="main-navbar">
      <img src="@/assets/logo.png" alt="GetKlean Logo" class="nav-logo" />
      <div class="main-nav-links">
        <a href="#" :class="{ 'active-link': activeSection === 'home' }" @click="handleHomeClick">Home</a>
        <a href="#services-section" :class="{ 'active-link': activeSection === 'services-section' }" @click="handleServicesClick">Services</a>
        <a href="#testimonial-section" :class="{ 'active-link': activeSection === 'testimonial-section' }" @click="handleNavClick">Testimonial</a>
        <router-link to="/customers" :class="{ 'active-link': activeSection === 'customers' }">Customers</router-link> 
        <router-link to="/about" :class="{ 'active-link': activeSection === 'about' }">About US</router-link> 
        <router-link to="/contact" :class="{ 'active-link': activeSection === 'contact' }">Contact US</router-link>
      </div>
    </div>
    <router-view/>
  </div>
</template>

# Smooth scroll for anchor navigation
<script>
export default {
  data() {
    return {
      activeSection: 'home'
    }
  },
  methods: {
    handleHomeClick() {
      this.activeSection = 'home';
      window.scrollTo({ top: 0, behavior: 'smooth' });
    },
    handleNavClick(e) {
      e.preventDefault();
      this.activeSection = 'testimonial-section';
      const target = document.getElementById('testimonial-section');
      if (target) {
        this.slowScrollTo(target, 1200);
      }
    },
    handleServicesClick(e) {
      e.preventDefault();
      this.activeSection = 'services-section';
      const target = document.getElementById('services-section');
      if (target) {
        this.slowScrollTo(target, 1200);
      }
    },
    slowScrollTo(target, duration = 1200) {
      const start = window.scrollY;
      const end = target.getBoundingClientRect().top + window.scrollY;
      const change = end - start;
      const startTime = performance.now();
      function animateScroll(currentTime) {
        const elapsed = currentTime - startTime;
        const progress = Math.min(elapsed / duration, 1);
        window.scrollTo(0, start + change * easeInOutQuad(progress));
        if (progress < 1) {
          requestAnimationFrame(animateScroll);
        }
      }
      function easeInOutQuad(t) {
        return t < 0.5 ? 2 * t * t : -1 + (4 - 2 * t) * t;
      }
      requestAnimationFrame(animateScroll);
    }
  }
}
</script>
<style lang="scss">
/* Logo container for independent styling */
.logo-container {
  display: flex;
  align-items: center;
  padding-right: 24px;
  height: 88px;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

nav {
  background: #fff;
  box-shadow: 0 2px 8px rgba(0,0,0,0.05);
  padding: 0 40px;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 64px;
  gap: 32px;
  border-radius: 0;
  border: none;
}
nav .nav-links a,
nav .nav-links .router-link,
nav .nav-links .router-link-active,
nav .nav-links .router-link-exact-active {
  color: #fff !important;
}
nav .nav-links a {
  font-weight: 600;
  text-decoration: none;
  padding: 10px 22px;
  border-radius: 6px;
  transition: background 0.2s, color 0.2s;
  font-size: 1.3rem;
}
nav .nav-links a:hover,
nav .nav-links .router-link:hover {
  background: #f0f4f8;
  color: #42b983 !important;
}
nav .nav-links .router-link-exact-active {
  background: #42b983;
  color: #fff !important;
  box-shadow: 0 2px 8px rgba(66,185,131,0.10);
}
/* Navigation bar styling */
.navbar {
  display: flex;
  align-items: center;
  height: 88px;
  padding: 0 24px;
  background: 
#3c86c7;
  box-shadow: 0 2px 8px rgba(0,0,0,0.04);
}
.colorNav{
  background: 
#3c86c7;
}
.navbar nav {
  flex: 1;
  display: flex;
  justify-content: flex-start;
  height: 88px;
}
.nav-logo {
  height: 120px;
  max-height: 140px;
  width: 360px;
  min-width: 220px;
  border-radius: 6px;
  object-fit: contain;
  margin-right: 32px;
}
.nav-links {
  background: transparent;
  border: none;
  border-radius: 0;
  display: flex;
  gap: 32px;
  align-items: center;
  margin-left: 60px;
}
.main-navbar {
  display: flex;
  align-items: center;
  height: 88px;
  padding: 0 24px;
  background: #3c86c7;
  box-shadow: 0 2px 8px rgba(0,0,0,0.04);
  position: sticky;
  top: 0;
  z-index: 1000;
}
.main-nav-links {
  display: flex;
  gap: 32px;
  align-items: center;
  margin-left: 120px;
  /* You can adjust margin-right if you want more space from the edge */
}
.main-navbar .nav-logo {
  height: 120px;
  max-height: 140px;
  width: 360px;
  min-width: 220px;
  border-radius: 6px;
  object-fit: contain;
  margin-right: 32px;
}
.main-nav-links {
  display: flex;
  gap: 32px;
  align-items: center;
  /* You can adjust margin-left or flex here for alignment */
}
.main-nav-links a,
.main-nav-links .router-link,
.main-nav-links .router-link-active,
.main-nav-links .router-link-exact-active {
  color: #fff !important;
}
.main-nav-links a {
  font-weight: 600;
  text-decoration: none;
  padding: 10px 22px;
  border-radius: 6px;
  transition: background 0.2s, color 0.2s;
  font-size: 1.3rem;
}
.main-nav-links a:hover,
.main-nav-links .router-link:hover {
  background: #f0f4f8;
  color: #42b983 !important;
}
.main-nav-links .active-link,
.main-nav-links .router-link-exact-active {
  background: #42b983;
  color: #fff !important;
  box-shadow: 0 2px 8px rgba(66,185,131,0.10);
}
</style>
