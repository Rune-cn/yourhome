<script setup>
import { media } from '../data/media.js'

function pretty(u) {
  return u.replace(/^https?:\/\//, '').replace(/\/$/, '')
}
</script>

<template>
  <header class="hero">
    <span class="dot" aria-hidden="true"></span>
    <div class="rule" aria-hidden="true"></div>
    <h1 class="serif">Ilyfalt</h1>
    <p class="sub">
      一个由 <b>AI</b> 驱动的人类。这里是个人主页：入口、导航、以及一些随手做的小工具。
    </p>
    <nav class="media" aria-label="个人媒体">
      <a v-for="m in media" :key="m.name" :href="m.url" target="_blank" rel="noopener">
        <svg viewBox="0 0 16 16" fill="currentColor" aria-hidden="true">
          <path :d="m.icon" />
        </svg>
        <span>{{ m.name }}</span>
      </a>
    </nav>
  </header>
</template>

<style scoped>
.hero {
  min-height: 62vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  padding: 4.5rem clamp(1.4rem, 6vw, 5.5rem) 3rem;
  position: relative;
}

.rule {
  width: 56px;
  height: 4px;
  background: var(--accent);
  margin-bottom: 2.2rem;
  border-radius: 2px;
}

h1 {
  font-size: clamp(3rem, 11vw, 7rem);
  font-weight: 700;
  letter-spacing: 0.01em;
  line-height: 1.02;
}

.sub {
  margin-top: 1.4rem;
  max-width: 34em;
  color: var(--text-dim);
  font-size: clamp(1rem, 2.4vw, 1.25rem);
}

.sub b {
  color: var(--accent);
  font-weight: 600;
}

.media {
  display: flex;
  flex-wrap: wrap;
  gap: 0.9rem 1.6rem;
  margin-top: 2.6rem;
  font-size: 0.98rem;
}

.media a {
  color: var(--text-dim);
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  transition: color 0.18s ease;
}

.media a:hover {
  color: var(--accent);
}

.media svg {
  width: 1.05rem;
  height: 1.05rem;
  flex: none;
}

.dot {
  position: absolute;
  right: clamp(1.4rem, 6vw, 5.5rem);
  top: 4.5rem;
  width: 12px;
  height: 12px;
  border-radius: 50%;
  background: var(--blue);
  opacity: 0.85;
}
</style>
