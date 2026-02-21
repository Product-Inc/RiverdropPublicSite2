<script setup lang="ts">
useSeoMeta({
  title: 'Docs | Riverdrop',
  description: 'Riverdrop documentation highlights for implementation, formats, customization, and data collection.'
})

const sections = [
  {
    title: 'Implementation',
    body: 'Embed experiences with a lightweight script and configure launch behavior for your site architecture.'
  },
  {
    title: 'Formats',
    body: 'Use full-screen, widget, and promo units depending on campaign placement and content layout.'
  },
  {
    title: 'Administration',
    body: 'Review results, access user-level exports, and approve/edit/publish content from the admin interface.'
  },
  {
    title: 'Data collection',
    body: 'Collect aggregate and user-level data with CSV downloads or JSON delivery to partner endpoints.'
  }
]
</script>

<template>
  <section class="section container page-hero">
    <h1>Docs</h1>
    <p>Everything your team needs to launch and optimize Riverdrop experiences.</p>
  </section>

  <section class="section section-soft">
    <div class="container card-grid card-grid-2">
      <article v-for="item in sections" :key="item.title" class="feature-card">
        <h3>{{ item.title }}</h3>
        <p>{{ item.body }}</p>
      </article>
    </div>
  </section>

  <section class="section container">
    <h2>Quick start snippet</h2>
    <pre class="code-block"><code>&lt;script src="https://cdn.riverdrop.com/embed.js"&gt;&lt;/script&gt;
&lt;div id="riverdrop-experience" data-format="widget"&gt;&lt;/div&gt;</code></pre>
  </section>
</template>
