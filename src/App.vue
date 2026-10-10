
<script setup>
import { ref } from 'vue'

const menuOpen = ref(false)

const skills = [
  { name: 'C', level: 'Programming', icon: 'C' },
  { name: 'C++', level: 'Programming', icon: 'C++' },
  { name: 'HTML & CSS', level: 'Web Development', icon: '</>' },
  { name: 'JavaScript', level: 'Programming', icon: 'JS' },
  { name: 'Python', level: 'Programming', icon: 'Py' },
  { name: 'Arduino', level: 'Embedded Systems', icon: '⌘' },
  { name: 'SQL', level: 'Database', icon: 'DB' },
  { name: 'Git & GitHub', level: 'Version Control', icon: 'Git' }
]

const projects = [
  {
    number: '01',
    title: 'E-Sentriq Laboratory Monitoring System',
    category: 'Academic Project · System Development',
    description:
      'A proposed monitoring system for organizing records, tracking equipment or resources, and supporting more efficient management.',
    tags: ['System Design', 'Database', 'Monitoring'],
    symbol: '▦'
  },
  {
    number: '02',
    title: 'Embedded Systems Projects',
    category: 'Academic Projects · Electronics',
    description:
      'Hands-on projects involving microcontrollers, electronic components, sensors, and basic hardware-software integration.',
    tags: ['C/C++', 'Arduino', 'Electronics'],
    symbol: '⌘'
  }
]

const achievements = [
  {
    year: 'Academic',
    title: 'Computer Engineering Projects',
    description:
      'Completed academic activities involving programming, electronics, system design, and technical problem-solving.'
  },
  {
    year: 'Research',
    title: 'Sentriq Thesis Development',
    description:
      'Contributing to the design and development of a smart laboratory equipment storage and access control system.'
  },
]

const contact = {
  address: 'Accusilian, Tuao, Cagayan',
  phone: '09457622190',
  email: 'raiyyanmaniago45@gmail.com'
}

const closeMenu = () => {
  menuOpen.value = false
}
</script>

<template>
  <div class="portfolio">
    <!-- Navigation -->
    <header class="navbar">
      <a class="brand" href="#home" @click="closeMenu">
        <span class="brand-icon">R</span>
        <span>RAIYYAN<span class="brand-dot">.</span></span>
      </a>

      <button
        class="menu-toggle"
        type="button"
        aria-label="Toggle navigation"
        :aria-expanded="menuOpen"
        @click="menuOpen = !menuOpen"
      >
        {{ menuOpen ? '✕' : '☰' }}
      </button>

      <nav class="nav-links" :class="{ 'nav-open': menuOpen }">
        <a href="#home" @click="closeMenu">Home</a>
        <a href="#about" @click="closeMenu">About</a>
        <a href="#skills" @click="closeMenu">Skills</a>
        <a href="#projects" @click="closeMenu">Projects</a>
        <a href="#achievements" @click="closeMenu">Achievements</a>
        <a href="#contact" @click="closeMenu">Contact</a>
        <a
          class="nav-cv"
          href="/cv.pdf"
          download="Raiyyan_Maniago_CV.pdf"
          @click="closeMenu"
        >
          ↓ Download CV
        </a>
      </nav>
    </header>

    <main>
      <!-- Hero -->
      <section id="home" class="hero section-wrap">
        <div class="hero-content">
          <div class="availability">
            <span class="status-dot"></span>
            COMPUTER ENGINEERING STUDENT
          </div>

          <p class="eyebrow">HELLO, WELCOME TO MY PORTFOLIO</p>

          <h1>
            Hi, I'm <span class="accent-text">Raiyyan</span>
            <br />
            Maniago<span class="accent-text">.</span>
          </h1>

          <h2 class="hero-subtitle">
            Aspiring Computer Engineer
          </h2>

          <p class="hero-description">
            I am a Computer Engineering student interested in programming,
            embedded systems, and technology. I enjoy learning how hardware
            and software work together to solve real-world problems. I also like cats and lizards
          </p>

          <div class="hero-buttons">
            <a href="#projects" class="button button-primary">
              Existing Projects <span>↗</span>
            </a>

            <a
              href="/cv.pdf"
              class="button button-outline"
              download="Raiyyan_Maniago_CV.pdf"
            >
              <span>↓</span> Download CV
            </a>
          </div>

          <div class="hero-details">
            <div class="detail-item">
              <span class="detail-icon">⌖</span>
              <span>Philippines</span>
            </div>
            <div class="detail-item">
              <span class="detail-icon">⌘</span>
              <span>Computer Engineering</span>
            </div>
          </div>
        </div>

        <div class="hero-visual">
          <div class="photo-glow"></div>
          <div class="photo-frame">
            <img
              src="/profile.jfif"
              alt="Portrait of Raiyyan Maniago"
              class="profile-photo"
            />
          </div>

          <div class="photo-caption">
            <span class="caption-line"></span>
            <div>
              <p class="caption-title">CURIOUS BY NATURE</p>
              <p class="caption-subtitle">Building. Learning. Improving.</p>
            </div>
          </div>

          <div class="floating-card floating-card-top">
            <span class="floating-symbol">&lt;/&gt;</span>
            <div>
              <strong>Code</strong>
              <small>Think & Create</small>
            </div>
          </div>

          <div class="floating-card floating-card-bottom">
            <span class="floating-symbol">⌘</span>
            <div>
              <strong>Engineering</strong>
              <small>Ideas into solutions</small>
            </div>
          </div>
        </div>

        <a class="scroll-indicator" href="#about">
          <span class="scroll-line"></span>
          SCROLL TO EXPLORE
        </a>
      </section>

      <!-- About -->
      <section id="about" class="section section-wrap">
        <div class="section-heading">
          <p class="eyebrow">GET TO KNOW ME</p>
          <h2>About <span class="accent-text">Me</span></h2>
          <p class="section-intro">
            A little about my background, interests, and goals.
          </p>
        </div>

        <div class="about-grid">
          <div class="about-mark">
            <div class="about-circle">
              <span class="about-letter">R</span>
              <span class="circle-caption">LEARN · BUILD · GROW</span>
            </div>
            <span class="decor-leaf leaf-one">✳</span>
            <span class="decor-leaf leaf-two">✦</span>
          </div>

          <div class="about-copy">
            <h3>Technology with purpose.</h3>
            <p>
              I am an aspiring Computer Engineer who wants to develop
              practical technical skills and create useful technology-based
              solutions. My interests include computer programming,
              electronics, embedded systems, and system development.
            </p>
            <p>
              Through academic projects and hands-on activities, I continue
              to develop my problem-solving skills, learn new technologies,
              and understand how engineering concepts can be applied to
              everyday challenges.
            </p>

            <div class="about-facts">
              <div class="fact">
                <span class="fact-symbol">⌘</span>
                <div>
                  <strong>Technical Learning</strong>
                  <small>Programming and electronics</small>
                </div>
              </div>
              <div class="fact">
                <span class="fact-symbol">✧</span>
                <div>
                  <strong>Problem Solving</strong>
                  <small>Practical and creative thinking</small>
                </div>
              </div>
              <div class="fact">
                <span class="fact-symbol">⌁</span>
                <div>
                  <strong>Continuous Growth</strong>
                  <small>Learning through experience</small>
                </div>
              </div>
            </div>
          </div>
        </div>
      </section>

      <!-- Skills -->
      <section id="skills" class="section skills-section">
        <div class="section-wrap">
          <div class="section-heading">
            <p class="eyebrow">WHAT I WORK WITH</p>
            <h2>My <span class="accent-text">Skills</span></h2>
            <p class="section-intro">
              Technologies and tools I am learning and using in my projects.
            </p>
          </div>

          <div class="skills-grid">
            <article
              v-for="skill in skills"
              :key="skill.name"
              class="skill-card"
            >
              <div class="skill-icon">{{ skill.icon }}</div>
              <div>
                <h3>{{ skill.name }}</h3>
                <p>{{ skill.level }}</p>
              </div>
              <span class="skill-arrow">↗</span>
            </article>
          </div>

          <div class="skills-note">
            <span class="note-icon">✳</span>
            <p>
              I am continuously improving these skills through coursework,
              practice, and personal and academic projects.
            </p>
          </div>
        </div>
      </section>

      <!-- Projects -->
      <section id="projects" class="section section-wrap">
        <div class="section-heading">
          <p class="eyebrow">SOME THINGS I'VE WORKED ON</p>
          <h2>Featured <span class="accent-text">Projects</span></h2>
          <p class="section-intro">
            Academic work and technical projects that reflect my interests.
          </p>
        </div>

        <div class="projects-grid">
          <article
            v-for="project in projects"
            :key="project.number"
            class="project-card"
          >
            <div class="project-top">
              <span class="project-number">{{ project.number }}</span>
              <span class="project-symbol">{{ project.symbol }}</span>
            </div>

            <p class="project-category">{{ project.category }}</p>
            <h3>{{ project.title }}</h3>
            <p class="project-description">{{ project.description }}</p>

            <div class="project-tags">
              <span v-for="tag in project.tags" :key="tag">{{ tag }}</span>
            </div>
          </article>
        </div>

        <p class="projects-disclaimer">
          Note: Project descriptions can be updated to reflect the final
          features, implementation, and contributions of each project.
        </p>
      </section>

      <!-- Achievements and Certificates -->
      <section id="achievements" class="section achievements-section">
        <div class="section-wrap">
          <div class="section-heading">
            <p class="eyebrow">MY LEARNING JOURNEY</p>
            <h2>Achievements & <span class="accent-text">Certificates</span></h2>
            <p class="section-intro">
              Experiences and milestones that contribute to my growth.
            </p>
          </div>

          <div class="timeline">
            <article
              v-for="(achievement, index) in achievements"
              :key="achievement.title"
              class="timeline-item"
            >
              <div class="timeline-marker">
                <span>{{ String(index + 1).padStart(2, '0') }}</span>
              </div>

              <div class="timeline-card">
                <span class="timeline-year">{{ achievement.year }}</span>
                <h3>{{ achievement.title }}</h3>
                <p>{{ achievement.description }}</p>
              </div>
            </article>
          </div>

          <div class="certificate-note">
            <span class="certificate-icon">✧</span>
            <div>
              <h3>Certificates and Recognition</h3>
              <p>
                Civil Service Professional Level Passer
              </p>
            </div>
          </div>
        </div>
      </section>

      <!-- Contact -->
      <section id="contact" class="section section-wrap">
        <div class="contact-panel">
          <div class="contact-copy">
            <p class="eyebrow">LET'S CONNECT</p>
            <h2>Have a project or an idea in mind?</h2>
            <p>
              Feel free to reach out for any queries regarding academic collaborations, project
              discussions, or opportunities to learn and grow.
            </p>
            <a
              :href="`mailto:${contact.email}`"
              class="button button-primary contact-cta"
            >
              Send Me an Email <span>↗</span>
            </a>
          </div>

          <div class="contact-list">
            <a :href="`mailto:${contact.email}`" class="contact-item">
              <span class="contact-icon">✉</span>
              <span class="contact-text">
                <small>EMAIL ADDRESS</small>
                <strong>{{ contact.email }}</strong>
              </span>
              <span class="contact-arrow">↗</span>
            </a>

            <a :href="`tel:${contact.phone}`" class="contact-item">
              <span class="contact-icon">☏</span>
              <span class="contact-text">
                <small>PHONE NUMBER</small>
                <strong>{{ contact.phone }}</strong>
              </span>
              <span class="contact-arrow">↗</span>
            </a>

            <div class="contact-item">
              <span class="contact-icon">⌖</span>
              <span class="contact-text">
                <small>LOCATION</small>
                <strong>{{ contact.address }}</strong>
              </span>
            </div>
          </div>
        </div>
      </section>
    </main>

    <!-- Footer -->
    <footer class="footer">
      <a class="brand footer-brand" href="#home">
        <span class="brand-icon">R</span>
        <span>RAIYYAN<span class="brand-dot">.</span></span>
      </a>

      <p>Designed with purpose. Built with curiosity.</p>

      <a href="#home" class="back-to-top">
        BACK TO TOP ↑
      </a>

      <p class="copyright">
        © {{ new Date().getFullYear() }} Raiyyan Maniago. All rights reserved.
      </p>
    </footer>
  </div>
</template>

<style>
@import url('https://fonts.googleapis.com/css2?family=DM+Sans:wght@400;500;600;700&family=Manrope:wght@400;500;600;700;800&display=swap');

:root {
  --forest-950: #091a14;
  --forest-900: #0c2119;
  --forest-800: #123528;
  --forest-700: #1d4a36;
  --forest-600: #2c6549;
  --moss: #8eae79;
  --lime: #c4df9a;
  --cream: #f3f2e9;
  --muted: #a4b5a8;
  --line: rgba(196, 223, 154, 0.16);
  --card: rgba(255, 255, 255, 0.035);
}

* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

html {
  scroll-behavior: smooth;
  scroll-padding-top: 90px;
}

body {
  background: var(--forest-950);
  color: var(--cream);
  font-family: 'DM Sans', sans-serif;
  line-height: 1.7;
}

a {
  color: inherit;
  text-decoration: none;
}

button {
  font: inherit;
}

button,
a {
  -webkit-tap-highlight-color: transparent;
}

::selection {
  background: var(--lime);
  color: var(--forest-950);
}

.portfolio {
  min-height: 100vh;
  overflow: hidden;
  background:
    radial-gradient(
      ellipse at 85% 10%,
      rgba(44, 101, 73, 0.13),
      transparent 35%
    ),
    var(--forest-950);
}

.section-wrap {
  width: min(1160px, calc(100% - 64px));
  margin-inline: auto;
}

/* Navigation */

.navbar {
  position: sticky;
  top: 0;
  z-index: 100;
  display: flex;
  align-items: center;
  justify-content: space-between;
  min-height: 82px;
  padding: 0 max(32px, calc((100% - 1160px) / 2));
  border-bottom: 1px solid rgba(255, 255, 255, 0.055);
  background: rgba(9, 26, 20, 0.91);
  backdrop-filter: blur(18px);
}

.brand {
  display: inline-flex;
  align-items: center;
  gap: 11px;
  font-family: 'Manrope', sans-serif;
  font-size: 14px;
  font-weight: 800;
  letter-spacing: 2px;
}

.brand-icon {
  display: grid;
  width: 35px;
  height: 35px;
  place-items: center;
  border: 1px solid rgba(196, 223, 154, 0.48);
  border-radius: 10px 3px 10px 3px;
  background: rgba(196, 223, 154, 0.09);
  color: var(--lime);
  font-size: 17px;
}

.brand-dot,
.accent-text {
  color: var(--lime);
}

.nav-links {
  display: flex;
  align-items: center;
  gap: 25px;
}

.nav-links > a:not(.nav-cv) {
  color: #bdc9bf;
  font-size: 12px;
  transition: color 0.2s ease;
}

.nav-links > a:not(.nav-cv):hover {
  color: var(--lime);
}

.nav-cv {
  display: inline-flex;
  align-items: center;
  gap: 8px;
  padding: 10px 15px;
  border: 1px solid rgba(196, 223, 154, 0.4);
  border-radius: 6px;
  color: var(--lime);
  font-size: 12px;
  font-weight: 700;
  transition: background 0.2s ease, color 0.2s ease;
}

.nav-cv:hover {
  background: var(--lime);
  color: var(--forest-950);
}

.menu-toggle {
  display: none;
  border: 0;
  background: transparent;
  color: var(--cream);
  cursor: pointer;
  font-size: 24px;
}

/* Hero */

.hero {
  position: relative;
  display: grid;
  grid-template-columns: 1.05fr 0.95fr;
  align-items: center;
  gap: 60px;
  min-height: 670px;
  padding-top: 85px;
  padding-bottom: 125px;
}

.hero-content {
  position: relative;
  z-index: 2;
}

.availability {
  display: inline-flex;
  align-items: center;
  gap: 9px;
  margin-bottom: 30px;
  padding: 7px 12px;
  border: 1px solid var(--line);
  border-radius: 30px;
  background: rgba(196, 223, 154, 0.035);
  color: #c4d2c4;
  font-size: 9px;
  font-weight: 700;
  letter-spacing: 1.5px;
}

.status-dot {
  width: 7px;
  height: 7px;
  border-radius: 50%;
  background: var(--lime);
  box-shadow: 0 0 10px rgba(196, 223, 154, 0.6);
}

.eyebrow {
  margin-bottom: 13px;
  color: var(--moss);
  font-size: 10px;
  font-weight: 700;
  letter-spacing: 3px;
}

.hero h1,
.section-heading h2,
.contact-copy h2 {
  font-family: 'Manrope', sans-serif;
  font-weight: 800;
  letter-spacing: -2px;
}

.hero h1 {
  font-size: clamp(46px, 6vw, 74px);
  line-height: 1.12;
}

.hero-subtitle {
  margin-top: 22px;
  color: #d1decf;
  font-family: 'Manrope', sans-serif;
  font-size: 19px;
  font-weight: 500;
}

.hero-description {
  max-width: 490px;
  margin-top: 19px;
  color: var(--muted);
  font-size: 14px;
  line-height: 1.95;
}

.hero-buttons {
  display: flex;
  flex-wrap: wrap;
  gap: 13px;
  margin-top: 31px;
}

.button {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  gap: 13px;
  min-height: 47px;
  padding: 0 19px;
  border: 1px solid transparent;
  border-radius: 5px;
  font-size: 12px;
  font-weight: 700;
  transition:
    transform 0.2s ease,
    background 0.2s ease,
    border-color 0.2s ease;
}

.button:hover {
  transform: translateY(-3px);
}

.button-primary {
  background: var(--lime);
  color: var(--forest-950);
}

.button-primary:hover {
  background: #d5eab6;
}

.button-outline {
  border-color: rgba(196, 223, 154, 0.35);
  color: var(--cream);
}

.button-outline:hover {
  border-color: var(--lime);
  background: rgba(196, 223, 154, 0.07);
}

.hero-details {
  display: flex;
  flex-wrap: wrap;
  gap: 23px;
  margin-top: 42px;
}

.detail-item {
  display: flex;
  align-items: center;
  gap: 9px;
  color: #aab9ad;
  font-size: 11px;
}

.detail-icon {
  color: var(--lime);
  font-size: 17px;
}

.hero-visual {
  position: relative;
  display: flex;
  align-items: center;
  justify-content: center;
  min-height: 400px;
}

.photo-glow {
  position: absolute;
  width: 340px;
  height: 340px;
  border-radius: 50%;
  background: rgba(90, 138, 89, 0.17);
  filter: blur(45px);
}

.photo-frame {
  position: relative;
  z-index: 1;
  width: min(350px, 100%);
  height: 420px;
  padding: 10px;
  border: 1px solid rgba(196, 223, 154, 0.32);
  border-radius: 165px 165px 12px 12px;
  background: linear-gradient(
    150deg,
    rgba(196, 223, 154, 0.16),
    rgba(255, 255, 255, 0.015)
  );
  box-shadow: 0 30px 100px rgba(0, 0, 0, 0.2);
}

.profile-photo {
  display: block;
  width: 100%;
  height: 100%;
  border-radius: 155px 155px 7px 7px;
  object-fit: cover;
  object-position: center;
  background: var(--forest-800);
}

.photo-caption {
  position: absolute;
  right: 2px;
  bottom: -35px;
  z-index: 2;
  display: flex;
  align-items: center;
  gap: 12px;
}

.caption-line {
  width: 30px;
  height: 1px;
  background: var(--lime);
}

.caption-title {
  color: var(--cream);
  font-size: 9px;
  font-weight: 700;
  letter-spacing: 1.6px;
}

.caption-subtitle {
  margin-top: 3px;
  color: var(--muted);
  font-size: 10px;
}

.floating-card {
  position: absolute;
  z-index: 3;
  display: flex;
  align-items: center;
  gap: 10px;
  padding: 13px 16px;
  border: 1px solid rgba(196, 223, 154, 0.18);
  border-radius: 8px;
  background: rgba(15, 40, 29, 0.95);
  box-shadow: 0 12px 30px rgba(0, 0, 0, 0.2);
}

.floating-card-top {
  top: 55px;
  left: -10px;
}

.floating-card-bottom {
  right: -10px;
  bottom: 30px;
}

.floating-symbol {
  display: grid;
  width: 34px;
  height: 34px;
  place-items: center;
  border-radius: 6px;
  background: rgba(196, 223, 154, 0.1);
  color: var(--lime);
  font-size: 14px;
  font-weight: 700;
}

.floating-card strong,
.floating-card small {
  display: block;
}

.floating-card strong {
  font-size: 11px;
}

.floating-card small {
  margin-top: 2px;
  color: var(--muted);
  font-size: 9px;
}

.scroll-indicator {
  position: absolute;
  bottom: 40px;
  left: 0;
  display: flex;
  align-items: center;
  gap: 12px;
  color: #84998a;
  font-size: 9px;
  font-weight: 700;
  letter-spacing: 2px;
}

.scroll-line {
  width: 35px;
  height: 1px;
  background: var(--moss);
}

/* General sections */

.section {
  padding-top: 100px;
  padding-bottom: 100px;
}

.section-heading {
  margin-bottom: 45px;
}

.section-heading h2 {
  font-size: clamp(32px, 4vw, 45px);
  line-height: 1.25;
}

.section-intro {
  max-width: 560px;
  margin-top: 13px;
  color: var(--muted);
  font-size: 13px;
}

/* About */

.about-grid {
  display: grid;
  grid-template-columns: 0.8fr 1.2fr;
  align-items: center;
  gap: 85px;
}

.about-mark {
  position: relative;
  display: grid;
  min-height: 330px;
  place-items: center;
}

.about-circle {
  position: relative;
  display: flex;
  width: 250px;
  height: 250px;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  border: 1px solid rgba(196, 223, 154, 0.38);
  border-radius: 50%;
  background:
    radial-gradient(
      circle at 40% 35%,
      rgba(79, 125, 81, 0.27),
      transparent 65%
    ),
    rgba(255, 255, 255, 0.015);
  box-shadow:
    0 0 0 13px rgba(196, 223, 154, 0.025),
    0 0 0 26px rgba(196, 223, 154, 0.015);
}

.about-letter {
  color: var(--lime);
  font-family: 'Manrope', sans-serif;
  font-size: 100px;
  font-weight: 800;
  line-height: 1;
}

.circle-caption {
  margin-top: 12px;
  color: var(--muted);
  font-size: 8px;
  letter-spacing: 2px;
}

.decor-leaf {
  position: absolute;
  color: var(--moss);
}

.leaf-one {
  top: 30px;
  right: 22px;
  font-size: 33px;
}

.leaf-two {
  bottom: 45px;
  left: 30px;
  color: var(--lime);
  font-size: 25px;
}

.about-copy h3 {
  margin-bottom: 15px;
  font-family: 'Manrope', sans-serif;
  font-size: 24px;
  font-weight: 700;
}

.about-copy > p {
  margin-bottom: 15px;
  color: var(--muted);
  font-size: 13px;
  line-height: 1.95;
}

.about-facts {
  display: grid;
  grid-template-columns: repeat(2, minmax(0, 1fr));
  gap: 20px 15px;
  margin-top: 30px;
}

.fact {
  display: flex;
  align-items: center;
  gap: 11px;
}

.fact-symbol {
  display: grid;
  width: 38px;
  height: 38px;
  flex-shrink: 0;
  place-items: center;
  border: 1px solid var(--line);
  border-radius: 8px;
  color: var(--lime);
}

.fact strong,
.fact small {
  display: block;
}

.fact strong {
  font-size: 11px;
}

.fact small {
  margin-top: 3px;
  color: var(--muted);
  font-size: 9px;
}

/* Skills */

.skills-section,
.achievements-section {
  border-top: 1px solid rgba(255, 255, 255, 0.04);
  border-bottom: 1px solid rgba(255, 255, 255, 0.04);
  background:
    radial-gradient(
      ellipse at 50% 0%,
      rgba(44, 101, 73, 0.1),
      transparent 65%
    ),
    rgba(255, 255, 255, 0.012);
}

.skills-grid {
  display: grid;
  grid-template-columns: repeat(4, minmax(0, 1fr));
  gap: 15px;
}

.skill-card {
  position: relative;
  display: flex;
  min-height: 112px;
  align-items: center;
  gap: 13px;
  padding: 18px;
  border: 1px solid rgba(196, 223, 154, 0.12);
  border-radius: 8px;
  background: var(--card);
  transition:
    transform 0.2s ease,
    border-color 0.2s ease,
    background 0.2s ease;
}

.skill-card:hover {
  transform: translateY(-4px);
  border-color: rgba(196, 223, 154, 0.4);
  background: rgba(196, 223, 154, 0.045);
}

.skill-icon {
  display: grid;
  width: 43px;
  height: 43px;
  flex-shrink: 0;
  place-items: center;
  border-radius: 7px;
  background: rgba(196, 223, 154, 0.1);
  color: var(--lime);
  font-family: 'Manrope', sans-serif;
  font-size: 12px;
  font-weight: 800;
}

.skill-card h3 {
  font-size: 12px;
  font-weight: 700;
}

.skill-card p {
  margin-top: 4px;
  color: var(--muted);
  font-size: 10px;
}

.skill-arrow {
  position: absolute;
  top: 12px;
  right: 13px;
  color: #66836d;
  font-size: 12px;
}

.skills-note {
  display: flex;
  align-items: flex-start;
  gap: 12px;
  margin-top: 25px;
  padding: 17px 20px;
  border-left: 2px solid var(--moss);
  background: rgba(196, 223, 154, 0.035);
}

.note-icon {
  color: var(--lime);
}

.skills-note p {
  color: var(--muted);
  font-size: 11px;
}

/* Projects */

.projects-grid {
  display: grid;
  grid-template-columns: repeat(3, minmax(0, 1fr));
  gap: 18px;
}

.project-card {
  display: flex;
  min-height: 330px;
  flex-direction: column;
  padding: 25px;
  border: 1px solid rgba(196, 223, 154, 0.13);
  border-radius: 9px;
  background: var(--card);
  transition:
    transform 0.2s ease,
    border-color 0.2s ease;
}

.project-card:hover {
  transform: translateY(-5px);
  border-color: rgba(196, 223, 154, 0.38);
}

.project-top {
  display: flex;
  align-items: center;
  justify-content: space-between;
  margin-bottom: 26px;
}

.project-number {
  color: #7f9982;
  font-family: 'Manrope', sans-serif;
  font-size: 11px;
  letter-spacing: 2px;
}

.project-symbol {
  display: grid;
  width: 48px;
  height: 48px;
  place-items: center;
  border: 1px solid var(--line);
  border-radius: 10px;
  background: rgba(196, 223, 154, 0.07);
  color: var(--lime);
  font-size: 26px;
}

.project-category {
  margin-bottom: 8px;
  color: var(--moss);
  font-size: 9px;
  font-weight: 600;
}

.project-card h3 {
  font-family: 'Manrope', sans-serif;
  font-size: 19px;
  font-weight: 700;
}

.project-description {
  margin-top: 13px;
  color: var(--muted);
  font-size: 12px;
  line-height: 1.9;
}

.project-tags {
  display: flex;
  flex-wrap: wrap;
  gap: 7px;
  margin-top: auto;
  padding-top: 24px;
}

.project-tags span {
  padding: 5px 8px;
  border: 1px solid rgba(196, 223, 154, 0.13);
  border-radius: 4px;
  color: #bdcbbb;
  font-size: 9px;
}

.projects-disclaimer {
  margin-top: 20px;
  color: #84a78e;
  font-size: 10px;
}

/* Achievements */

.timeline {
  max-width: 850px;
  margin-inline: auto;
}

.timeline-item {
  display: grid;
  grid-template-columns: 55px 1fr;
  gap: 18px;
  padding-bottom: 22px;
}

.timeline-marker {
  position: relative;
  display: flex;
  justify-content: center;
}

.timeline-marker::after {
  position: absolute;
  top: 45px;
  bottom: -22px;
  width: 1px;
  background: rgba(196, 223, 154, 0.18);
  content: '';
}

.timeline-item:last-child .timeline-marker::after {
  display: none;
}

.timeline-marker span {
  display: grid;
  width: 42px;
  height: 42px;
  place-items: center;
  border: 1px solid rgba(196, 223, 154, 0.28);
  border-radius: 50%;
  background: var(--forest-900);
  color: var(--lime);
  font-size: 10px;
  font-weight: 700;
}

.timeline-card {
  padding: 20px 24px;
  border: 1px solid rgba(196, 223, 154, 0.12);
  border-radius: 8px;
  background: var(--card);
}

.timeline-year {
  color: var(--moss);
  font-size: 9px;
  font-weight: 700;
  letter-spacing: 1.5px;
  text-transform: uppercase;
}

.timeline-card h3 {
  margin-top: 5px;
  font-family: 'Manrope', sans-serif;
  font-size: 16px;
}

.timeline-card p {
  margin-top: 7px;
  color: var(--muted);
  font-size: 12px;
  line-height: 1.9;
}

.certificate-note {
  display: flex;
  align-items: flex-start;
  gap: 17px;
  max-width: 850px;
  margin: 22px auto 0;
  padding: 22px;
  border: 1px dashed rgba(196, 223, 154, 0.25);
  border-radius: 8px;
}

.certificate-icon {
  color: var(--lime);
  font-size: 25px;
}

.certificate-note h3 {
  font-size: 13px;
}

.certificate-note p {
  margin-top: 5px;
  color: var(--muted);
  font-size: 11px;
}

/* Contact */

.contact-panel {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 65px;
  padding: 48px;
  border: 1px solid rgba(196, 223, 154, 0.2);
  border-radius: 12px;
  background:
    radial-gradient(
      ellipse at 0% 100%,
      rgba(44, 101, 73, 0.23),
      transparent 60%
    ),
    rgba(255, 255, 255, 0.025);
}

.contact-copy h2 {
  max-width: 440px;
  font-size: clamp(29px, 3.5vw, 42px);
  line-height: 1.3;
}

.contact-copy > p:not(.eyebrow) {
  max-width: 410px;
  margin-top: 18px;
  color: var(--muted);
  font-size: 12px;
  line-height: 1.95;
}

.contact-cta {
  margin-top: 25px;
}

.contact-list {
  display: flex;
  flex-direction: column;
  justify-content: center;
  gap: 12px;
}

.contact-item {
  display: flex;
  align-items: center;
  gap: 14px;
  min-width: 0;
  padding: 16px;
  border: 1px solid rgba(196, 223, 154, 0.12);
  border-radius: 7px;
  background: rgba(255, 255, 255, 0.025);
}

a.contact-item {
  transition: border-color 0.2s ease, background 0.2s ease;
}

a.contact-item:hover {
  border-color: rgba(196, 223, 154, 0.35);
  background: rgba(196, 223, 154, 0.04);
}

.contact-icon {
  display: grid;
  width: 39px;
  height: 39px;
  flex-shrink: 0;
  place-items: center;
  border-radius: 7px;
  background: rgba(196, 223, 154, 0.1);
  color: var(--lime);
  font-size: 18px;
}

.contact-text {
  display: block;
  min-width: 0;
}

.contact-text small,
.contact-text strong {
  display: block;
  overflow-wrap: anywhere;
}

.contact-text small {
  margin-bottom: 3px;
  color: #8fa792;
  font-size: 8px;
  font-weight: 700;
  letter-spacing: 1.4px;
}

.contact-text strong {
  color: var(--cream);
  font-size: 11px;
  font-weight: 500;
}

.contact-arrow {
  margin-left: auto;
  color: var(--moss);
}

/* Footer */

.footer {
  display: grid;
  grid-template-columns: 1fr 1.4fr 1fr;
  align-items: center;
  gap: 20px;
  margin-top: 40px;
  padding: 28px max(32px, calc((100% - 1160px) / 2));
  border-top: 1px solid rgba(255, 255, 255, 0.06);
}

.footer > p:not(.copyright) {
  color: var(--muted);
  font-size: 10px;
  text-align: center;
}

.back-to-top {
  justify-self: end;
  color: var(--moss);
  font-size: 9px;
  font-weight: 700;
  letter-spacing: 1px;
}

.copyright {
  grid-column: 1 / -1;
  padding-top: 18px;
  border-top: 1px solid rgba(255, 255, 255, 0.05);
  color: #728778;
  font-size: 10px;
  text-align: center;
}

/* Responsive layout */

@media (max-width: 1000px) {
  .navbar {
    padding-inline: 25px;
  }

  .nav-links {
    gap: 15px;
  }

  .nav-links > a:not(.nav-cv) {
    font-size: 11px;
  }

  .hero {
    gap: 35px;
  }

  .photo-frame {
    width: 300px;
    height: 380px;
  }

  .floating-card-top {
    left: -5px;
  }

  .floating-card-bottom {
    right: -5px;
  }

  .skills-grid {
    grid-template-columns: repeat(2, minmax(0, 1fr));
  }

  .contact-panel {
    gap: 30px;
    padding: 35px;
  }
}

@media (max-width: 760px) {
  .section-wrap {
    width: min(100% - 38px, 550px);
  }

  .navbar {
    min-height: 72px;
    padding-inline: 20px;
  }

  .menu-toggle {
    display: block;
  }

  .nav-links {
    position: absolute;
    top: 71px;
    right: 0;
    left: 0;
    display: none;
    align-items: stretch;
    gap: 0;
    padding: 12px 20px 22px;
    border-bottom: 1px solid var(--line);
    background: rgba(9, 26, 20, 0.98);
  }

  .nav-links.nav-open {
    display: flex;
    flex-direction: column;
  }

  .nav-links > a:not(.nav-cv) {
    padding: 12px 4px;
    border-bottom: 1px solid rgba(255, 255, 255, 0.05);
    font-size: 13px;
  }

  .nav-cv {
    justify-content: center;
    margin-top: 13px;
  }

  .hero {
    grid-template-columns: 1fr;
    gap: 65px;
    padding-top: 70px;
    padding-bottom: 110px;
  }

  .hero-content {
    order: 1;
  }

  .hero-visual {
    order: 0;
    min-height: 350px;
  }

  .photo-frame {
    width: 265px;
    height: 335px;
  }

  .photo-glow {
    width: 270px;
    height: 270px;
  }

  .floating-card-top {
    top: 35px;
    left: max(0px, calc(50% - 185px));
  }

  .floating-card-bottom {
    right: max(0px, calc(50% - 185px));
    bottom: 12px;
  }

  .photo-caption {
    right: max(0px, calc(50% - 185px));
    bottom: -35px;
  }

  .hero h1 {
    font-size: clamp(43px, 10vw, 65px);
  }

  .scroll-indicator {
    bottom: 40px;
  }

  .section {
    padding-top: 75px;
    padding-bottom: 75px;
  }

  .about-grid {
    grid-template-columns: 1fr;
    gap: 35px;
  }

  .about-mark {
    min-height: 270px;
  }

  .about-circle {
    width: 210px;
    height: 210px;
  }

  .about-letter {
    font-size: 80px;
  }

  .about-facts {
    grid-template-columns: 1fr;
  }

  .projects-grid {
    grid-template-columns: 1fr;
  }

  .project-card {
    min-height: 285px;
  }

  .contact-panel {
    grid-template-columns: 1fr;
    gap: 35px;
    padding: 25px;
  }

  .footer {
    grid-template-columns: 1fr 1fr;
    padding-inline: 20px;
  }

  .footer > p:not(.copyright) {
    display: none;
  }

  .back-to-top {
    justify-self: end;
  }
}

@media (max-width: 420px) {
  .section-wrap {
    width: calc(100% - 32px);
  }

  .availability {
    font-size: 8px;
    letter-spacing: 1px;
  }

  .hero-buttons {
    align-items: stretch;
    flex-direction: column;
  }

  .hero-buttons .button {
    width: 100%;
  }

  .hero-details {
    gap: 12px;
  }

  .skills-grid {
    grid-template-columns: 1fr;
  }

  .skill-card {
    min-height: 90px;
  }

  .timeline-item {
    grid-template-columns: 42px 1fr;
    gap: 10px;
  }

  .timeline-marker span {
    width: 35px;
    height: 35px;
  }

  .timeline-marker::after {
    top: 38px;
  }

  .timeline-card {
    padding: 16px;
  }

  .contact-panel {
    padding: 20px 15px;
  }

  .contact-item {
    gap: 10px;
    padding: 12px;
  }

  .contact-text strong {
    font-size: 10px;
  }

  .footer {
    gap: 15px;
  }
}
</style>
