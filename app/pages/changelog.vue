<script setup lang="ts">
useSeoMeta({
  title: 'Changelog | Riverdrop',
  description: 'Riverdrop product release notes and platform updates.'
})

const updates = [
  {
    date: '2026-02-20',
    title: 'Public site + Cloud Run auto-deploy',
    body: 'Launched the Riverdrop public marketing site with automated deployment from GitHub to Cloud Run.'
  },
  {
    date: '2026-02-12',
    title: 'Enhanced publish controls',
    body: 'Added clearer review and publish states for quiz and poll workflows in the admin product.'
  },
  {
    date: '2026-01-28',
    title: 'Template workflow improvements',
    body: 'Expanded template support for branded quiz and poll experiences with faster setup.'
  }
]
</script>

<template>
  <section class="section container page-hero">
    <h1>Changelog</h1>
    <p>Recent updates across Riverdrop platform and delivery workflows.</p>
  </section>

  <section class="section section-soft">
    <div class="container timeline-list">
      <article v-for="item in updates" :key="item.date + item.title" class="timeline-item">
        <p class="timeline-date">{{ item.date }}</p>
        <h3>{{ item.title }}</h3>
        <p>{{ item.body }}</p>
      </article>
    </div>
  </section>
</template>
