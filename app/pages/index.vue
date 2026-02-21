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

const highlights = [
  {
    icon: '⚡',
    title: 'AI-generated from your content',
    body: 'Riverdrop creates engaging quiz and poll questions from your published pages and can auto-refresh as new content goes live.'
  },
  {
    icon: '🎯',
    title: 'Built for engagement + conversion',
    body: 'Players can compete, share results, and sign up for notifications to keep returning to your experiences.'
  },
  {
    icon: '🧠',
    title: 'Partner-controlled workflows',
    body: 'Teams can approve, edit, and publish with controls that fit editorial and growth operations.'
  },
  {
    icon: '📈',
    title: 'Data-driven growth',
    body: 'Track visitors, engagement, and outcomes over time with aggregate analytics and user-level export options.'
  }
]

const logos = ['AP', 'PBS', 'Gannett', 'Trusted Media Brands', 'MarketWatch', 'Benzinga']

const games = [
  { name: 'Quizzes', state: 'Available now', icon: '✅' },
  { name: 'Polls', state: 'Available now', icon: '✅' },
  { name: 'Surveys', state: 'Available now', icon: '✅' },
  { name: 'Timeline', state: 'Coming soon', icon: '🕒' },
  { name: 'Strands', state: 'Coming soon', icon: '🧵' },
  { name: 'Decision Tree', state: 'Coming soon', icon: '🌿' },
  { name: 'Image Match', state: 'Coming soon', icon: '🖼️' }
]

const benefits = [
  'Full-screen, widget, and promotional formats for different placements',
  'Partner branding and sponsor integration across gameplay and results',
  'User sharing prompts and optional email/text notifications',
  'Advertising support for native, display, and interstitial units',
  'CSV and JSON data access for analysis and downstream workflows'
]
</script>

<template>
  <section class="hero container" id="top">
    <p class="eyebrow">Marketing Platform for Publishers and SaaS Teams</p>
    <h1>Drive growth with AI-driven casual games based on your content</h1>
    <p class="subheader">
      Build audience and grow revenue by creating quizzes, polls and other games unique to your content and brand.
    </p>
    <div class="hero-actions">
      <a class="btn btn-primary" href="#contact">Get Started</a>
      <NuxtLink class="btn btn-ghost" to="/product">Explore Product</NuxtLink>
    </div>
  </section>

  <section class="section section-soft">
    <div class="container">
      <h2>Trusted by leading media and content brands</h2>
      <div class="logo-row">
        <div v-for="company in logos" :key="company" class="logo-pill">{{ company }}</div>
      </div>
    </div>
  </section>

  <section class="section container" id="features">
    <h2>Built from real Riverdrop platform capabilities</h2>
    <div class="card-grid card-grid-4">
      <article v-for="item in highlights" :key="item.title" class="feature-card colorful">
        <div class="icon-chip">{{ item.icon }}</div>
        <h3>{{ item.title }}</h3>
        <p>{{ item.body }}</p>
      </article>
    </div>
  </section>

  <section class="section section-soft">
    <div class="container two-col">
      <div>
        <h2>Feature depth from Riverdrop.Quiz</h2>
        <p>
          Riverdrop supports the full lifecycle from automatic generation to controlled publishing, with privacy-first data controls and monetization options.
        </p>
        <ul class="clean-list">
          <li v-for="item in benefits" :key="item">{{ item }}</li>
        </ul>
      </div>
      <div class="image-stack">
        <img src="/media/ap_news_quiz.png" alt="Riverdrop quiz card example" />
        <img src="/media/newschallenge_promo.png" alt="Riverdrop promotional unit example" />
      </div>
    </div>
  </section>

  <section class="section container">
    <h2>Game library</h2>
    <p class="section-intro">Launch today with quizzes, polls, and surveys. More formats are on the roadmap.</p>
    <div class="card-grid card-grid-4">
      <article v-for="game in games" :key="game.name" class="game-card">
        <p class="game-icon">{{ game.icon }}</p>
        <h3>{{ game.name }}</h3>
        <p :class="game.state === 'Available now' ? 'state-live' : 'state-soon'">{{ game.state }}</p>
      </article>
    </div>
  </section>

  <section class="section section-soft">
    <div class="container">
      <h2>See Riverdrop in action</h2>
      <div class="media-grid">
        <figure class="media-card">
          <img src="/media/riverdropquiz.png" alt="Riverdrop product screenshot" />
          <figcaption>Interactive product experience</figcaption>
        </figure>
        <figure class="media-card">
          <img src="/media/ap_sports_quiz.png" alt="Riverdrop sports quiz example" />
          <figcaption>Publisher-ready game output</figcaption>
        </figure>
        <figure class="media-card media-video">
          <video src="/media/reel.mp4" controls muted playsinline preload="metadata"></video>
          <figcaption>Riverdrop platform video</figcaption>
        </figure>
      </div>
    </div>
  </section>

  <section class="section container centered-copy" id="contact">
    <h2>Ready to turn your content into growth?</h2>
    <p>Start building branded AI-driven games that increase engagement and revenue.</p>
    <a class="btn btn-primary" href="mailto:hello@riverdrop.com">Contact Sales</a>
  </section>
</template>
