# Test Mike Docs

This repository tests **multi-versioned documentation** using **MkDocs** and **Mike**, with automated deployment via **GitHub Actions**.

## 📚 Documentation

- **[Latest stable version](https://czoido.github.io/test-mike/latest/)**
- **[Development version](https://czoido.github.io/test-mike/dev/)** (updated on each push to `main`)

## 🔄 Versioning Strategy

- Only the **latest patch of each minor version** is kept.
- **Examples:**
  - If `0.1.2` is released, `0.1.1` is removed.
  - If `1.2.4` is released, `1.2.3` is removed.
- The `latest` alias always points to the most recent stable version.

## 🚀 Deployment Process

- **Stable releases (`latest`)**  
  - Triggered by a **GitHub Release**.  
  - Removes previous patches of the same version series (`X.Y.Z`).  

- **Development (`dev`)**  
  - Triggered on **push to `main`**.  
