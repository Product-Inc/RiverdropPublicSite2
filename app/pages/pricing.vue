<script setup lang="ts">
useSeoMeta({
  title: 'Pricing | Riverdrop',
  description: 'Simple Riverdrop pricing for teams launching AI-powered quizzes, polls, and interactive games.'
})

const plans = [
  {
    name: 'Starter',
    price: '$499/mo',
    points: ['1 brand workspace', 'Quizzes, polls, surveys', 'Basic analytics', 'Email support']
  },
  {
    name: 'Growth',
    price: '$1,499/mo',
    points: ['Multi-format campaigns', 'Approvals + publishing workflows', 'Data export + webhook delivery', 'Priority support']
  },
  {
    name: 'Enterprise',
    price: 'Custom',
    points: ['Custom formats + integrations', 'Advanced ad/sponsorship support', 'Security and governance controls', 'Dedicated success manager']
  }
]
</script>

<template>
  <section class="section container page-hero">
    <h1>Pricing</h1>
    <p>Choose a plan that matches your audience and publishing velocity.</p>
  </section>

  <section class="section section-soft">
    <div class="container card-grid card-grid-3">
      <article v-for="plan in plans" :key="plan.name" class="price-card">
        <h3>{{ plan.name }}</h3>
        <p class="price">{{ plan.price }}</p>
        <ul>
          <li v-for="point in plan.points" :key="point">{{ point }}</li>
        </ul>
      </article>
    </div>
  </section>

  <section class="section container centered-copy">
    <h2>Need volume-based or annual pricing?</h2>
    <p>We support tailored commercial terms for large publisher and media networks.</p>
    <a class="btn btn-primary" href="mailto:hello@riverdrop.com">Contact Sales</a>
  </section>
</template>
