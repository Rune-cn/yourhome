<template>
  <footer>
    <span class="f-label">友链</span>
    <a href="https://gohugo.io/" target="_blank" rel="noopener">Hugo 官网</a>
  </footer>
</template>

<style scoped>
footer {
  border-top: 1px solid var(--line);
  padding: 1.8rem clamp(1.4rem, 6vw, 5.5rem);
  color: var(--text-dim);
  font-size: 0.88rem;
  display: flex;
  align-items: center;
  gap: 0.8rem;
  flex-wrap: wrap;
}
.f-label {
  color: var(--text-dim);
}
a {
  color: var(--blue);
}
a:hover {
  color: var(--accent);
}
</style>
