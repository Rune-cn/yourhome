<script setup>
import { sites } from '../data/sites.js'

function pretty(u) {
  return u.replace(/^https?:\/\//, '').replace(/\/$/, '')
}
</script>

<template>
  <main class="grid-wrap">
    <p class="section-label">精选站点与工具</p>
    <div class="grid">
      <a
        v-for="(s, i) in sites"
        :key="s.url"
        class="card"
        :href="s.url"
        target="_blank"
        rel="noopener"
        :aria-label="`${s.name}：${s.desc}`"
      >
        <h3>
          <span class="idx" aria-hidden="true">{{ String(i + 1).padStart(2, '0') }}</span>
          {{ s.name }}
        </h3>
        <p>{{ s.desc }}</p>
        <span class="url">{{ pretty(s.url) }}</span>
      </a>
    </div>
  </main>
</template>

<style scoped>
.grid-wrap {
  padding: 1rem clamp(1.4rem, 6vw, 5.5rem) 4.5rem;
}

.section-label {
  font-size: 0.86rem;
  color: var(--text-dim);
  margin-bottom: 1.4rem;
  letter-spacing: 0.04em;
}

.grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
  gap: 1px;
  background: var(--line);
  border: 1px solid var(--line);
}

.card {
  background: var(--bg-soft);
  padding: 1.3rem 1.3rem 1.2rem;
  min-height: 128px;
  display: flex;
  flex-direction: column;
  gap: 0.5rem;
  transition: background 0.18s ease;
}

.card:hover,
.card:focus-visible {
  background: var(--surface);
  outline: none;
}

.card h3 {
  font-size: 1.05rem;
  font-weight: 600;
  display: flex;
  align-items: baseline;
  gap: 0.5rem;
}

.card h3 .idx {
  color: var(--accent);
  font-size: 0.82rem;
}

.card p {
  color: var(--text-dim);
  font-size: 0.9rem;
  line-height: 1.55;
  flex: 1;
}

.card .url {
  color: var(--blue);
  font-size: 0.82rem;
  word-break: break-all;
  opacity: 0.9;
}

.card:hover .url {
  opacity: 1;
}
</style>
