<script setup lang="ts">
useSeoMeta({
  title: 'Blog | Riverdrop',
  description: 'Insights and updates from Riverdrop on audience growth, interactive content, and AI-driven games.'
})

const posts = [
  {
    title: 'How media brands use quizzes to increase repeat sessions',
    excerpt: 'Practical patterns for pairing editorial content with interactive formats that keep users engaged.'
  },
  {
    title: 'Designing sponsorship-ready casual games',
    excerpt: 'How to package branded touchpoints across gameplay, results, and leaderboard moments.'
  },
  {
    title: 'From content URL to launch: AI game generation workflow',
    excerpt: 'A behind-the-scenes look at Riverdrop’s generation, review, and publish pipeline.'
  }
]
</script>

<template>
  <section class="section container page-hero">
    <h1>Blog</h1>
    <p>Guides and ideas for content-led growth teams using Riverdrop.</p>
  </section>

  <section class="section section-soft">
    <div class="container card-grid card-grid-1">
      <article v-for="post in posts" :key="post.title" class="feature-card">
        <h3>{{ post.title }}</h3>
        <p>{{ post.excerpt }}</p>
      </article>
    </div>
  </section>
</template>
