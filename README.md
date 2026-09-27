# YourHome · 个人主页

基于 **Vue 3 + Vite** 的纯静态个人主页：个人简介、媒体链接、站点导航网格。

## 目录结构

```
yourhome/
├── index.html              # HTML 入口
├── vite.config.js          # Vite 配置
├── package.json
├── src/
│   ├── main.js             # 应用入口
│   ├── style.css           # 全局样式与设计令牌
│   ├── App.vue             # 根组件
│   ├── data/
│   │   ├── sites.js        # 站点/工具列表（改这里）
│   │   └── media.js        # 个人媒体链接（改这里）
│   └── components/
│       ├── HeroSection.vue # 顶部 Hero
│       ├── SiteGrid.vue    # 站点网格
│       └── FooterBar.vue   # 页脚
```

## 开发

```bash
npm install
npm run dev      # 本地预览
npm run build    # 构建到 dist/
npm run preview  # 预览构建产物
```

## 部署

`npm run build` 后把 `dist/` 目录上传到任意静态托管（Cloudflare Pages / GitHub Pages / Vercel 等）。

## 定制

- 站点列表：编辑 `src/data/sites.js`
- 媒体链接：编辑 `src/data/media.js`
- 配色与字体：编辑 `src/style.css` 与各组件 `<style>`

## 许可证

[MIT](LICENSE)
