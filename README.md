# 🚀 Releases Repository

This repository contains **production-ready build artifacts** for various projects in the ConC portfolio ecosystem.  
It is intentionally separated from source code to provide a clean, secure, and deployment-friendly structure.

> ⚠️ No development files live here. This repo only hosts *compiled*, *static*, and *deployable* content.

---

## 🗂 Structure

releases/
├── portfolio-site/       # Built output of the Vue/Vite-based portfolio
├── v86-terminal/         # Static Linux kernel + v86 WASM boot files
├── shared-assets/        # Favicons, fonts, theme assets
└── README.md

Each top-level directory corresponds to a standalone project or deployable unit.

---

## 🔐 Security Philosophy

This repo follows a **hard separation between development and deployment**:

- No source files, env vars, or sensitive material
- No scripts, build tools, or package dependencies
- No GitHub Actions tokens or writable secrets

Only finalized, tested, and intentionally exported assets are published here.

---

## 📦 Deployment Targets

This repository is suitable for:
- GitHub Pages
- Cloudflare Pages
- Static hosting/CDN
- Archive mirroring

Each subproject may include its own `.html` entry point and routing rules.

---

## 🔄 Update Flow

> All build artifacts are committed manually or by script.

1. Build in source project:
   ```bash
   npm run build

	2.	Copy to this repo:

rsync -a dist/ ../releases/portfolio-site/


	3.	Commit + push:

git commit -am "🚀 Deploy new portfolio build"
git push origin main

