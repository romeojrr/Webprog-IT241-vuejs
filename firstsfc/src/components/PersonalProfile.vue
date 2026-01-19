<template>
  <div class="personal-profile">
    <nav id="main-nav" class="navbar navbar-expand-lg fixed-top navbar-dark">
        <div class="container">
            <a class="navbar-brand fw-bold" href="#">My Personal Website<span>.</span></a>
            <div class="collapse navbar-collapse" id="navbarNav">
                <ul class="navbar-nav ms-auto">
                    <li class="nav-item"><a class="nav-link" href="#home">Home</a></li>
                    <li class="nav-item"><a class="nav-link" href="#about">About Me</a></li>
                </ul>
            </div>
        </div>
    </nav>

    <section id="home" class="min-vh-100 d-flex align-items-center section-hero">
        <div class="container">
            <div class="row align-items-center">
                <div class="col-lg-6">
                    <h5 class="display-8 mb-3">Hello... I am</h5>
                    <h1 class="display-5 fw-bold mb-3">Romeo Albeza Jr.</h1>
                    <h2 class="h4 mb-4">
                        <span class="text-white fw-bold">{{ typewrittenText }}</span><span class="cursor">|</span>
                    </h2>
                    <h5 class="display-8 mb-3">"Just a chill guy surviving this cruel world"</h5>
                </div>
                <div class="col-lg-6 text-center">
                    <img src="/romeopogi.jpg" class="img-fluid profile-img" alt="Profile">
                </div>
            </div>
        </div>
    </section>

    <section id="about" class="py-5">
      <div class="container">
        <div class="glass-card p-4">
          <h3>About Me</h3>
          <p>My nickname is Leo. Coffee & Matcha Lover.</p>
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
    };
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
/* Paste your CSS here */
.personal-profile {
  background: linear-gradient(to right, #310b2d, #030200);
  color: #edd9ce;
}
.glass-card {
  background: rgba(255, 255, 255, 0.05);
  border-radius: 16px;
  border: 1px solid rgba(255, 255, 255, 0.1);
}
.profile-img {
  width: 300px;
  border-radius: 50%;
}
.cursor { animation: blink 1s infinite; }
@keyframes blink { 0%, 100% { opacity: 1; } 50% { opacity: 0; } }
</style>