## BioCAsia Website Deployment Guide

This guide documents how to set up and deploy the BioCAsia website using GitHub and Netlify.

---

### 🧬 1. Fork & Clone the Template

1. **Fork** the [BioC_template](https://github.com/Bioconductor/BioC_template.git) (or another preferred template).
2. **Rename** your forked repo (e.g. `BioCAsia2025`).
3. **Clone** it locally:

---

### 2. Make Website Edits

Update:

* `config.toml` or `config.yaml` with new conference details
* Homepage and markdown content in `/content/` and `/layouts/`
* Add or remove talks/workshops/sponsors as needed

Test locally (if Hugo is used):

```bash
hugo serve
```
### 3. Transfer Ownership to Bioconductor

* Go to your GitHub repo: https://github.com/YourUsername/BioCAsia2025
* Click Settings > scroll to Danger Zone > Transfer Ownership

---

### 4. Create Netlify Site

1. Go to [https://app.netlify.com](https://app.netlify.com)
2. Log in with GitHub
3. Click **“Add new site” > “Import an existing project”**
4. Select your conference repo
5. Build website

Netlify will build and host the site at a temporary URL like `biocasia2025.netlify.app`.

---
### 5. Route53 DNS Setup (Handled by Bioconductor)

The Bioconductor AWS admin will:

* Add a **CNAME record** pointing `biocasia2025.bioconductor.org` to the Netlify subdomain
* Or configure an **A record** depending on the setup

Once DNS propagates, the domain will be live.

---

### 6. Add Custom Domain

1. In Netlify, go to **Site settings > Domain management**
2. Click **“Add custom domain”**
3. Enter: `biocasia2025.bioconductor.org`

---

Go to your webiste! It takes a few minutes for your domain to be secure.
