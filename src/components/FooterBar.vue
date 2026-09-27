<template>
  <footer>
    <span>Ilyfalt · 由 Vue 构建的纯静态主页</span>
    <span>
      <a href="https://github.com/Rune-cn/" target="_blank" rel="noopener">GitHub</a>
      ·
      <a href="https://afdian.com/a/CNRune" target="_blank" rel="noopener">爱发电</a>
      ·
      <a href="https://space.bilibili.com/3546928530852407" target="_blank" rel="noopener">bilibili</a>
    </span>
  </footer>
</template>

<style scoped>
footer {
  border-top: 1px solid var(--line);
  padding: 2.2rem clamp(1.4rem, 6vw, 5.5rem);
  color: var(--text-dim);
  font-size: 0.88rem;
  display: flex;
  justify-content: space-between;
  flex-wrap: wrap;
  gap: 0.6rem;
}

footer a:hover {
  color: var(--accent);
}
</style>
