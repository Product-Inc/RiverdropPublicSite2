<script setup lang="ts">
const links = [
  { label: 'Product', to: '/product' },
  { label: 'Pricing', to: '/pricing' },
  { label: 'Docs', to: '/docs' },
  { label: 'Blog', to: '/blog' },
  { label: 'Changelog', to: '/changelog' }
]
</script>

<template>
  <div class="site-shell">
    <header class="site-header">
      <div class="container header-row">
        <NuxtLink to="/" class="brand-link" aria-label="Riverdrop Home">
          <img class="brand-logo" src="/icon-blue-500.svg" alt="Riverdrop logo" />
          <span>Riverdrop</span>
        </NuxtLink>

        <nav class="global-nav" aria-label="Global menu">
          <NuxtLink v-for="link in links" :key="link.to" :to="link.to">{{ link.label }}</NuxtLink>
        </nav>

        <div class="header-actions">
          <a class="btn btn-ghost" href="https://dashboard.riverdrop.com">Login</a>
          <NuxtLink class="btn btn-primary" to="/#contact">Get Started</NuxtLink>
        </div>
      </div>
    </header>

    <main>
      <slot />
    </main>

    <footer class="site-footer">
      <div class="container footer-row">
        <p>© {{ new Date().getFullYear() }} Riverdrop. All rights reserved.</p>
        <div class="footer-links">
          <NuxtLink to="/docs">Docs</NuxtLink>
          <NuxtLink to="/changelog">Changelog</NuxtLink>
        </div>
      </div>
    </footer>
  </div>
</template>
