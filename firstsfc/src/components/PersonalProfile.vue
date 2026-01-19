<template>
  <div class="personal-website-wrapper">
    <nav id="main-nav" class="navbar navbar-expand-lg fixed-top navbar-dark">
      <div class="container">
        <a class="navbar-brand fw-bold" href="#">My Personal Website<span class="dot">.</span></a>
        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav">
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarNav">
          <ul class="navbar-nav ms-auto">
            <li class="nav-item"><a class="nav-link" href="#home">Home</a></li>
            <li class="nav-item"><a class="nav-link" href="#about">About Me</a></li>
            <li class="nav-item"><a class="nav-link" href="#experience">Experience</a></li>
            <li class="nav-item"><a class="nav-link" href="#projects">Projects</a></li>
            <li class="nav-item"><a class="nav-link" href="#gallery">Gallery</a></li>
            <li class="nav-item"><a class="nav-link" href="#goals">Goals</a></li>
          </ul>
        </div>
      </div>
    </nav>

    <section id="home" class="min-vh-100 d-flex align-items-center section-hero">
      <div class="container">
        <div class="row align-items-center">
          <div class="col-lg-6 order-2 order-lg-1">
            <h5 class="display-8 mb-3">Hello... I am</h5>
            <h1 class="display-5 fw-bold mb-3">Romeo Albeza Jr.</h1>
            <h2 class="h4 mb-4 text-secondary-custom">
              <span class="text-white fw-bold">{{ typewrittenText }}</span><span class="cursor">|</span>
            </h2>
            <h5 class="display-8 mb-3">"Just a chill guy surviving this cruel world"</h5>
            <div class="d-flex gap-3 mt-4">
              <a href="#about" class="btn btn-primary-custom">About Me</a>
            </div>
          </div>
          <div class="col-lg-6 order-1 order-lg-2 text-center mb-5 mb-lg-0">
            <div class="hero-image-wrapper">
              <img src="/romeopogi.jpg" class="img-fluid profile-img" alt="Profile Picture">
            </div>
          </div>
        </div>
      </div>
    </section>

    <section id="about" class="py-5">
      <div class="container py-5">
        <div class="row g-4">
          <div class="col-lg-4">
            <div class="glass-card h-100 p-4">
              <h3 class="mb-4 text-white">About Me</h3>
              <ul class="list-unstyled text-secondary-custom">
                <li>My nickname is Leo</li>
                <li>Coffee & Matcha Lover</li>
                <li>Favorite artists: Laufey, Beabadoobee, Taylor Swift</li>
              </ul>
            </div>
          </div>
          <div class="col-lg-4">
            <div class="glass-card h-100 p-4">
              <h3 class="mb-4 text-white">Education</h3>
              <ul class="list-unstyled text-secondary-custom">
                <li>2nd Year, BSIT - Asia Pacific College</li>
              </ul>
            </div>
          </div>
          <div class="col-lg-4">
            <div class="glass-card h-100 p-4">
              <h3 class="mb-4 text-white">Hobbies</h3>
              <ul class="list-unstyled text-secondary-custom">
                <li>Music, Workout, Anime & Manga</li>
              </ul>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section id="gallery" class="py-5">
      <div class="container py-5">
        <h2 class="display-5 fw-bold mb-5 text-center">Picture Gallery</h2>
        <div class="row g-4 justify-content-center">
          <div class="col-md-4"><img src="/Joyride.jpg" class="img-fluid rounded-4 gallery-img"></div>
          <div class="col-md-4"><img src="/Mabait.jpg" class="img-fluid rounded-4 gallery-img"></div>
          <div class="col-md-4"><img src="/Car.jpg" class="img-fluid rounded-4 gallery-img"></div>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  data() {
    return {
      typewrittenText: '',
      fullPhrase: "2nd Year, BSIT",
    }
  },
  mounted() {
    this.typeEffect();
  },
  methods: {
    typeEffect() {
      let i = 0;
      const timer = setInterval(() => {
        if (i < this.fullPhrase.length) {
          this.typewrittenText += this.fullPhrase.charAt(i);
          i++;
        } else {
          clearInterval(timer);
        }
      }, 150);
    }
  }
}
</script>

<style scoped>
.personal-website-wrapper {
  --bg-dark: #030200;
  --accent-purple: #310b2d;
  --text-light: #edd9ce;
  background: linear-gradient(to right, var(--accent-purple), var(--bg-dark));
  color: var(--text-light);
  min-height: 100vh;
}

.navbar { background: rgba(3, 2, 0, 0.8); backdrop-filter: blur(12px); }
.dot { color: #edd9ce; }
.text-secondary-custom { color: #edd9ce; opacity: 0.8; }

.profile-img {
  width: 360px;
  height: 360px;
  border-radius: 50%;
  object-fit: cover;
  border: 2px solid rgba(240, 231, 220, 0.2);
}

.glass-card {
  background: linear-gradient(to left, var(--accent-purple), var(--bg-dark));
  border: 1px solid rgba(255, 255, 255, 0.05);
  border-radius: 16px;
}

.gallery-img { border: 2px solid rgba(255,255,255,0.1); transition: 0.3s; }
.gallery-img:hover { transform: scale(1.02); }

.cursor { display: inline-block; animation: blink 1s infinite; }
@keyframes blink { 0%, 100% { opacity: 1; } 50% { opacity: 0; } }
</style>