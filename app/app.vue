<script setup lang="ts">
useSeoMeta({
  title: 'Riverdrop | AI-Driven Casual Games for Growth',
  description:
    'Drive growth with AI-driven casual games based on your content. Build audience and grow revenue by creating quizzes, polls, and branded interactive formats.',
  ogTitle: 'Riverdrop | AI-Driven Casual Games for Growth',
  ogDescription:
    'Build audience and grow revenue by creating quizzes, polls and other games unique to your content and brand.',
  twitterCard: 'summary_large_image'
})

const featureCards = [
  {
    title: 'Generate games from your content',
    body: 'Turn your articles, videos, and topic pages into ready-to-publish quizzes and polls with AI-assisted question generation.'
  },
  {
    title: 'Brand-safe templates',
    body: 'Use reusable templates with your voice, visuals, and rules to keep every experience aligned to your brand.'
  },
  {
    title: 'Publish and embed anywhere',
    body: 'Ship to your site quickly with embed code and publishing controls designed for editorial and marketing teams.'
  },
  {
    title: 'Actionable analytics',
    body: 'Track response volume, completion trends, and audience behavior to optimize engagement and monetization.'
  }
]

const functionality = [
  'AI-assisted quiz and poll creation from URLs and source content',
  'Question editing workflows and approval controls before publish',
  'Template management for branding and repeatable game formats',
  'Flexible publish states with preview, publish, and unpublish controls',
  'Audience response collection and performance analytics views',
  'Website embedding and campaign distribution support'
]

const outcomes = [
  {
    title: 'Grow audience engagement',
    body: 'Give visitors interactive experiences that increase dwell time and repeat visits.'
  },
  {
    title: 'Monetize attention better',
    body: 'Pair high-intent interactions with sponsorship and ad opportunities tied to your content strategy.'
  },
  {
    title: 'Move faster with less lift',
    body: 'Launch more campaigns with a lightweight workflow built for lean content and growth teams.'
  }
]
</script>

<template>
  <NuxtRouteAnnouncer />
  <div class="site">
    <header class="topbar">
      <div class="container topbar-inner">
        <div class="brand">Riverdrop</div>
        <a class="button button-ghost" href="#contact">Book a Demo</a>
      </div>
    </header>

    <main>
      <section class="hero container">
        <p class="eyebrow">Marketing Platform for Publishers and SaaS Teams</p>
        <h1>Drive growth with AI-driven casual games based on your content</h1>
        <p class="subheader">
          Build audience and grow revenue by creating quizzes, polls and other games unique to your content and brand.
        </p>
        <div class="hero-actions">
          <a class="button button-primary" href="#contact">Get Started</a>
          <a class="button button-ghost" href="#features">Explore Features</a>
        </div>
      </section>

      <section id="features" class="section container">
        <h2>Everything you need to launch high-performing interactive content</h2>
        <div class="grid four-up">
          <article v-for="item in featureCards" :key="item.title" class="card">
            <h3>{{ item.title }}</h3>
            <p>{{ item.body }}</p>
          </article>
        </div>
      </section>

      <section class="section section-alt">
        <div class="container split">
          <div>
            <h2>Built around Riverdrop’s real product workflows</h2>
            <p>
              Riverdrop helps teams go from source content to published game experiences with approval, publishing, and analytics built in.
            </p>
          </div>
          <ul class="checklist">
            <li v-for="item in functionality" :key="item">{{ item }}</li>
          </ul>
        </div>
      </section>

      <section class="section container">
        <h2>Why teams choose Riverdrop</h2>
        <div class="grid three-up">
          <article v-for="item in outcomes" :key="item.title" class="card">
            <h3>{{ item.title }}</h3>
            <p>{{ item.body }}</p>
          </article>
        </div>
      </section>

      <section class="section section-alt">
        <div class="container testimonial">
          <h2>Designed for content-led growth</h2>
          <p>
            “Riverdrop helps us launch engaging quizzes and polls in hours, not weeks. We keep our brand voice and get clear data on what content drives conversion.”
          </p>
          <p class="quote-byline">Head of Audience Growth</p>
        </div>
      </section>

      <section id="contact" class="section container cta">
        <h2>Ready to turn your content into growth?</h2>
        <p>Start building branded AI-driven games that increase engagement and revenue.</p>
        <a class="button button-primary" href="mailto:hello@riverdrop.com">Contact Sales</a>
      </section>
    </main>

    <footer class="footer">
      <div class="container footer-inner">
        <p>© {{ new Date().getFullYear() }} Riverdrop. All rights reserved.</p>
      </div>
    </footer>
  </div>
</template>

<style>
:root {
  color-scheme: light;
}

* {
  box-sizing: border-box;
}

body {
  margin: 0;
  font-family: Inter, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
  color: #0f172a;
  background: #ffffff;
}

.site {
  min-height: 100vh;
}

.container {
  width: min(1100px, calc(100% - 3rem));
  margin: 0 auto;
}

.topbar {
  position: sticky;
  top: 0;
  background: rgba(255, 255, 255, 0.92);
  border-bottom: 1px solid #e2e8f0;
  backdrop-filter: blur(8px);
  z-index: 20;
}

.topbar-inner {
  height: 72px;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.brand {
  font-size: 1.125rem;
  font-weight: 700;
}

.hero {
  text-align: center;
  padding: 6rem 0 4rem;
}

.eyebrow {
  margin: 0;
  color: #475569;
  font-weight: 600;
}

h1 {
  margin: 1rem auto;
  max-width: 900px;
  font-size: clamp(2rem, 5vw, 3.5rem);
  line-height: 1.1;
}

.subheader {
  margin: 0 auto;
  max-width: 780px;
  color: #334155;
  font-size: clamp(1rem, 2.3vw, 1.25rem);
}

.hero-actions {
  margin-top: 2rem;
  display: flex;
  justify-content: center;
  gap: 0.75rem;
  flex-wrap: wrap;
}

.section {
  padding: 4rem 0;
}

.section-alt {
  background: #f8fafc;
  border-top: 1px solid #e2e8f0;
  border-bottom: 1px solid #e2e8f0;
}

h2 {
  margin: 0 0 1.5rem;
  font-size: clamp(1.5rem, 3vw, 2.25rem);
}

h3 {
  margin: 0 0 0.65rem;
  font-size: 1.125rem;
}

p {
  margin: 0;
  color: #334155;
  line-height: 1.6;
}

.grid {
  display: grid;
  gap: 1rem;
}

.four-up {
  grid-template-columns: repeat(4, minmax(0, 1fr));
}

.three-up {
  grid-template-columns: repeat(3, minmax(0, 1fr));
}

.card {
  border: 1px solid #e2e8f0;
  border-radius: 14px;
  background: white;
  padding: 1.25rem;
}

.split {
  display: grid;
  grid-template-columns: 1.2fr 1fr;
  gap: 2rem;
  align-items: start;
}

.checklist {
  margin: 0;
  padding-left: 1.1rem;
  display: grid;
  gap: 0.65rem;
  color: #0f172a;
}

.testimonial {
  text-align: center;
  max-width: 840px;
}

.quote-byline {
  margin-top: 1rem;
  font-weight: 600;
  color: #0f172a;
}

.cta {
  text-align: center;
}

.cta p {
  margin-bottom: 1.2rem;
}

.button {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  border-radius: 10px;
  padding: 0.7rem 1rem;
  text-decoration: none;
  font-weight: 600;
}

.button-primary {
  background: #0f172a;
  color: #fff;
  border: 1px solid #0f172a;
}

.button-ghost {
  background: #fff;
  color: #0f172a;
  border: 1px solid #cbd5e1;
}

.footer {
  border-top: 1px solid #e2e8f0;
  padding: 1.25rem 0;
}

.footer-inner {
  text-align: center;
}

@media (max-width: 960px) {
  .four-up {
    grid-template-columns: repeat(2, minmax(0, 1fr));
  }

  .three-up {
    grid-template-columns: 1fr;
  }

  .split {
    grid-template-columns: 1fr;
  }
}

@media (max-width: 560px) {
  .four-up {
    grid-template-columns: 1fr;
  }

  .container {
    width: min(1100px, calc(100% - 2rem));
  }

  .hero {
    padding-top: 4.5rem;
  }
}
</style>
