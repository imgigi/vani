# Vani 作品集 - 部署目录

本文件夹为整理后的**单一可部署目录**，包含主页与三个案例项目，便于本地预览和后续部署。

## 目录结构

```
site/
├── index.html          # 主页（Vani Zheng 作品集）
├── index.tsx
├── package.json
├── vite.config.ts
├── tsconfig.json
├── jellycat/           # 项目 01 - Jellycat 案例
│   ├── index.html
│   └── ...
├── gucci/              # 项目 02 - Gucci 案例
│   ├── index.html
│   └── ...
└── mo-co/              # 项目 03 - MO&Co 案例
    ├── index.html
    └── ...
```

## 本地预览

- **方式一（推荐）**：用本地静态服务器打开本目录根目录，例如：
  - VS Code 安装 “Live Server” 后右键 `index.html` → Open with Live Server
  - 或在该目录执行：`npx serve .` 或 `python -m http.server 8080`
- **方式二**：若使用 Vite，在 `site` 目录下执行 `npm install` 与 `npm run dev`，从根路径访问。

## 跳转关系

- 主页 `index.html` 中「查看案例研究」指向：`jellycat/`、`gucci/`、`mo-co/`
- 各案例页顶部有「← 返回主页」链接，指向 `../`

## 部署

将整个 **site** 文件夹上传到服务器或静态托管（如 Vercel、Netlify、GitHub Pages）即可。

- 部署时以 **site 目录为网站根目录**，保证 `index.html` 在根路径，子路径为 `jellycat/`、`gucci/`、`mo-co/`。
- 若使用 Vite 构建，可在 `site` 下执行 `npm run build`，将生成的 `dist` 内容作为部署根目录。
