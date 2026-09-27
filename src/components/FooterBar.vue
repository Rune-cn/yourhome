<template>
  <footer>
    <span class="f-label">友链</span>
    <div class="links">
      <a href="https://gohugo.io/" target="_blank" rel="noopener">Hugo 官网</a>
    </div>
  </footer>
</template>

<style scoped>
footer {
  border-top: 1px solid var(--line);
  padding: 1.8rem clamp(1.4rem, 6vw, 5.5rem);
  display: flex;
  flex-direction: column;
  gap: 0.5rem;
}
.f-label {
  color: var(--text-dim);
  font-size: 0.88rem;
}
.links {
  display: flex;
  flex-wrap: wrap;
  column-gap: 1.2rem;
  row-gap: 0.4rem;
}
.links a {
  color: var(--text-dim);
  font-size: 0.88rem;
}
.links a:hover {
  color: var(--accent);
}
</style>
