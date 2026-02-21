<script setup lang="ts">
useSeoMeta({
  title: 'Product | Riverdrop',
  description: 'Explore Riverdrop platform capabilities for AI-generated quizzes, polls, surveys, and game experiences.'
})

const pillars = [
  {
    title: 'AI content generation',
    text: 'Create game-ready questions from published URLs and source content with models tuned for engagement.'
  },
  {
    title: 'Flexible formats',
    text: 'Launch full screen, widget, and promotional placements to match content templates and campaign goals.'
  },
  {
    title: 'Editorial controls',
    text: 'Approve, edit, publish, and unpublish experiences with workflows built for content and growth teams.'
  },
  {
    title: 'Data and monetization',
    text: 'Track engagement, export user data, integrate notifications, and run sponsorship or ad experiences.'
  }
]
</script>

<template>
  <section class="section container page-hero">
    <h1>Riverdrop Product</h1>
    <p>
      Riverdrop turns your content into interactive games that drive engagement, signups, and revenue with minimal ongoing lift.
    </p>
  </section>

  <section class="section section-soft">
    <div class="container card-grid card-grid-2">
      <article v-for="item in pillars" :key="item.title" class="feature-card">
        <h3>{{ item.title }}</h3>
        <p>{{ item.text }}</p>
      </article>
    </div>
  </section>

  <section class="section container media-showcase">
    <img src="/media/riverdropquiz.png" alt="Riverdrop quiz product interface" />
    <div>
      <h2>From content to launch in one workflow</h2>
      <p>
        Teams use Riverdrop to automatically create experiences as new content is published, customize game behavior, and distribute across web, newsletter, and social touchpoints.
      </p>
    </div>
  </section>
</template>
