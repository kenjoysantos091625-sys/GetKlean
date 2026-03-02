<template>
  <section class="testimonial-section" id="testimonial-section">
      <h2 class="testimonial-title">What Our Clients Say</h2>
      <div class="testimonial-cards">
        <div class="testimonial-card">
          <div class="testimonial-quote">&#8220;</div>
          <div class="testimonial-text">
            Problem solved. Unlike other service providers na basta lang mabugahan ng tubig yung unit para masabing malinis. From now on, GetKlean is our family go-to aircon service. Thank you very much!
          </div>
          <div class="testimonial-author">Johnson Tang</div>
        </div>
        <div class="testimonial-card">
          <div class="testimonial-quote">&#8220;</div>
          <div class="testimonial-text">
            I am very satisfied with the outcome of the cleaning of ate Nely and Dominic. It was superb! They really know what they are doing, very focused on their work. As an OC in terms of cleaning, it exceeded my expectations and you really fee the worth of the service you paid for. Definitely, I would recommend this to my friends and my clients. I’m looking forward again to book a cleaning service from you! For this, it was a 5-star. Thank you, GetKlean Team!
          </div>
          <div class="testimonial-author">Charlie A</div>
        </div>
        <div class="testimonial-card">
          <div class="testimonial-quote">&#8220;</div>
          <div class="testimonial-text">
            10/10 ratings for their dedication and hardwork. They rarely talk to each other because they are so busy doing such a great job at cleaning our house. We can’t help but to compare them and our cleaning experience to other cleaners we’ve hired before. GetKlean cleaners will go above and beyond our expectations.
          </div>
          <div class="testimonial-author">Raech May</div>
        </div>
      </div>
  </section>
</template>

<script>
export default {
  name: 'TestimonialView',
}
</script>

<style scoped>
.testimonial-section {
  background: #4390d1;
  padding: 40px 0 80px 0;
  min-height: 90vh;
  display: flex;
  flex-direction: column;
  align-items: center;
}
.testimonial-container {
  background: rgba(67,144,209,0.18);
  max-width: 1400px;
  margin: 0 auto;
  padding: 32px 24px 48px 24px;
  border-radius: 18px;
  box-shadow: 0 4px 32px rgba(0,0,0,0.10);
  width: 100%;
}
.testimonial-title {
  color: #fff;
  font-size: 4rem;
  font-weight: 600;
  text-align: center;
  margin-bottom: 48px;
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
}
.testimonial-cards {
  display: flex;
  justify-content: center;
  gap: 48px;
  flex-wrap: wrap;
  margin-top: 32px;
}
.testimonial-card {
  background: #fff;
  border-radius: 12px;
  box-shadow: 0 8px 32px rgba(0,0,0,0.12);
  width: 320px;
  min-height: 320px;
  padding: 32px 18px 24px 18px;
  display: flex;
  flex-direction: column;
  align-items: center;
  position: relative;
  transition: box-shadow 0.2s;
}
.testimonial-card:hover {
  box-shadow: 0 12px 48px rgba(67,144,209,0.18);
}
.testimonial-quote {
  color: #4390d1;
  font-size: 4rem;
  font-weight: 700;
  margin-bottom: 24px;
}
.testimonial-text {
  color: #4390d1;
  font-size: 1.2rem;
  text-align: left;
  margin-bottom: 40px;
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
}
.testimonial-author {
  color: #4390d1;
  font-size: 1.2rem;
  font-weight: 700;
  text-align: center;
  margin-top: auto;
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
}
</style>
