# 🚀 Releases Repository

This repository contains **production-ready build artifacts** for various projects in across my repos.  


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

