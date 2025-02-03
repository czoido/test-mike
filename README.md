# Test Mike Docs

This repository is a **testing ground** for **multi-versioned documentation** using **MkDocs** and **Mike**.  
It explores **automated versioning, deployment, and cleanup of old patch versions** using **GitHub Actions**.

## 🔥 Motivation

Managing documentation for multiple versions of a project can become complex over time.  
This repository automates the process of:
- **Generating and deploying multiple versions of documentation**.
- **Keeping only the latest patch release** (e.g., if `0.1.2` is released, `0.1.1` is removed).
- **Maintaining separate branches for stable (`latest`) and development (`dev`) documentation**.
- **Fully automating deployment through GitHub Actions**.

## 📚 Documentation Structure

The documentation is published in **GitHub Pages** at:  
👉 **[Latest stable version](https://czoido.github.io/test-mike/latest/)**  
👉 **[Development version](https://czoido.github.io/test-mike/dev/)**  

Each new **minor or major release (`X.Y.Z`) automatically replaces previous patch versions** of the same series:  
✅ `0.1.0` → `0.1.1` → `0.1.2` (only `0.1.2` remains)  
✅ `1.2.3` → `1.2.4` (only `1.2.4` remains)  
✅ `2.3.5` → (next patch will remove `2.3.5` when published)  

## 🚀 Automated Deployment Workflow

The deployment process is fully **automated via GitHub Actions**:

1. **Stable releases (`latest`)**  
   - When a **GitHub Release is created**, documentation is deployed.  
   - The **last patch version of each series is kept**, older patches are deleted.  
   - The `latest` alias is updated to point to the most recent release.

2. **Development documentation (`dev`)**  
   - On **every push to `main`**, the documentation is deployed to `dev/`.
