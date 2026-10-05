<script setup>
import { ref } from 'vue'
import profileImage from './assets/profile.jpg'

const activeSection = ref('home')

const scrollToSection = (id) => {
  activeSection.value = id

  document.getElementById(id)?.scrollIntoView({
    behavior: 'smooth',
    block: 'start'
  })
}

const navItems = [
  { id: 'home', label: 'Homepage' },
  { id: 'about', label: 'About Me' },
  { id: 'education', label: 'Education' },
  { id: 'news', label: 'News' },
  { id: 'publications', label: 'Publications' },
  { id: 'honors', label: 'Honors' }
]
</script>

<template>
  <div class="page">

    <!-- Navigation -->
    <header class="navbar">
      <div class="nav-inner">
        <button
          class="site-name"
          @click="scrollToSection('home')"
        >
          Qinyu Mao
        </button>

        <nav>
          <button
            v-for="item in navItems"
            :key="item.id"
            :class="{ active: activeSection === item.id }"
            @click="scrollToSection(item.id)"
          >
            {{ item.label }}
          </button>
        </nav>
      </div>
    </header>


    <main>

      <!-- =========================
           Homepage
      ========================== -->
      <section id="home" class="profile-section">

        <div class="profile-layout">

          <div class="profile-photo-wrapper">
            <img
              :src="profileImage"
              alt="Qinyu Mao"
              class="profile-photo"
            />
          </div>

          <div class="profile-info">

            <h1>Qinyu Mao</h1>

            <p class="subtitle">
              Graduate Student at Southeast University
            </p>

            <p class="research-line">
              Trustworthy AI · Intelligent Agents · Large Language Models
            </p>

            <p class="location">
              Nanjing, China
            </p>

            <div class="contact-links">
              <a href="mailto:your-email@example.com">
                Email
              </a>

              <a
                href="https://github.com/"
                target="_blank"
              >
                GitHub
              </a>

              <a
                href="#"
                target="_blank"
              >
                Google Scholar
              </a>
            </div>

          </div>

        </div>

        <div class="intro">
          <p>
            I am currently a graduate student at the School of Computer
            Science and Engineering, Southeast University. My research
            interests focus on trustworthy intelligent agents, large
            language models, and reliable AI systems.
          </p>

          <p>
            Previously, I received my Bachelor's degree from Xiangtan
            University, where I worked on artificial intelligence,
            deep learning, and biological network analysis.
          </p>

          <p>
            My research goal is to build AI systems that are not only
            capable, but also reliable, robust, interpretable, and
            trustworthy.
          </p>
        </div>

      </section>


      <!-- =========================
           About Me
      ========================== -->
      <section id="about" class="content-section">

        <h2>About Me</h2>

        <p>
          I am interested in the intersection of artificial intelligence,
          intelligent agents, and trustworthy machine learning.
        </p>

        <p>
          My current work explores how intelligent agents can reason,
          plan, use tools, and interact with complex environments while
          maintaining reliability and robustness.
        </p>

        <div class="research-tags">
          <span>Trustworthy AI</span>
          <span>LLM Agents</span>
          <span>Large Language Models</span>
          <span>Reliable AI</span>
          <span>Intelligent Systems</span>
        </div>

      </section>


      <!-- =========================
           Education
      ========================== -->
      <section id="education" class="content-section">

        <h2>🎓 Education</h2>

        <div class="timeline">

          <div class="timeline-item">
            <div class="timeline-date">
              2027 – Present
            </div>

            <div class="timeline-content">
              <h3>Southeast University</h3>

              <p>
                School of Computer Science and Engineering
              </p>

              <p class="muted">
                Graduate Student · Computer Science
              </p>

              <p class="tags">
                Trustworthy AI · AI Agents · Large Language Models
              </p>
            </div>
          </div>


          <div class="timeline-item">
            <div class="timeline-date">
              2023 – 2027
            </div>

            <div class="timeline-content">
              <h3>Xiangtan University</h3>

              <p>
                Undergraduate · Software Engineering
              </p>

              <p class="muted">
                Artificial Intelligence · Deep Learning
              </p>

              <p class="tags">
                AI · Deep Learning · Software Engineering
              </p>
            </div>
          </div>

        </div>

      </section>


      <!-- =========================
           News
      ========================== -->
      <section id="news" class="content-section">

        <h2>🔥 News</h2>

        <div class="news-list">

          <div class="news-item">
            <span class="news-date">2027</span>
            <span>
              Started my graduate study at Southeast University.
            </span>
          </div>

          <div class="news-item">
            <span class="news-date">2026</span>
            <span>
              Continued research on graph neural networks and
              disease-gene prediction.
            </span>
          </div>

          <div class="news-item">
            <span class="news-date">2025</span>
            <span>
              Research work on dynamic differential protein interaction
              networks was accepted by IEEE BIBM.
            </span>
          </div>

        </div>

      </section>


      <!-- =========================
           Publications
      ========================== -->
      <section id="publications" class="content-section">

        <h2>📝 Publications</h2>

        <div class="publication-list">

          <article class="publication">

            <div class="publication-year">
              2025
            </div>

            <div class="publication-body">

              <h3>
                Construction of Multiple Dynamic Differential
                Protein Interaction Networks for Identifying Disease Genes
              </h3>

              <p class="authors">
                Mao Q., Huang Z., Wen X., et al.
              </p>

              <p class="venue">
                IEEE International Conference on Bioinformatics
                and Biomedicine (BIBM), 2025
              </p>

              <div class="publication-links">
                <a href="#" target="_blank">
                  Paper
                </a>

                <a href="#" target="_blank">
                  Code
                </a>
              </div>

            </div>

          </article>


          <article class="publication">

            <div class="publication-year">
              2026
            </div>

            <div class="publication-body">

              <h3>
                DyFRP: Dynamic Network Rewiring and Graph
                Representation for Disease Gene Prediction
              </h3>

              <p class="authors">
                Qinyu Mao
              </p>

              <p class="venue">
                Ongoing Research
              </p>

              <div class="publication-links">
                <a href="#" target="_blank">
                  Project
                </a>

                <a href="#" target="_blank">
                  Code
                </a>
              </div>

            </div>

          </article>

        </div>

      </section>


      <!-- =========================
          Honors and Awards
      ========================== -->
      <section id="honors" class="content-section">

        <h2>Honors and Awards</h2>

        <ol class="honor-list">

          <li class="honor-item">
            <span>
              Second Prize, National Division, China Collegiate Computer Design Competition
            </span>
            <span class="honor-date">(2026.08)</span>
          </li>

          <li class="honor-item">
            <span>
              Second Prize, National Division, Lanqiao Cup Programming Competition
            </span>
            <span class="honor-date">(2026.06)</span>
          </li>

          <li class="honor-item">
            <span>
              First Prize, Provincial Division, China Collegiate Computer Design Competition
            </span>
            <span class="honor-date">(2026.05)</span>
          </li>

          <li class="honor-item">
            <span>
              First Prize, Provincial Division, Lanqiao Cup Programming Competition
            </span>
            <span class="honor-date">(2026.04)</span>
          </li>

        </ol>

      </section>

      <!-- =========================
           Contact
      ========================== -->
      <section class="contact-section">

        <h2>Contact</h2>

        <p>
          I am always open to discussing research ideas,
          collaborations, and interesting AI problems.
        </p>

        <a
          href="mailto:your-email@example.com"
          class="email-link"
        >
          your-email@example.com
        </a>

      </section>

    </main>


    <!-- Footer -->
    <footer>
      <p>
        © 2026 Qinyu Mao
      </p>

      <p>
        Built with Vue 3 · Vite · GitHub Pages
      </p>
    </footer>

  </div>
</template>