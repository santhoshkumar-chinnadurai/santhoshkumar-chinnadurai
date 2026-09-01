# GitHub Portfolio Deployment & Step-by-Step Rebuild Guide

This guide contains the exact steps to finalize your GitHub portfolio transformation.

---

## ⚡ Step 1: Activate Special GitHub Profile README

1. Open your browser and navigate to:  
   👉 **`https://github.com/santhoshkumar-chinnadurai/-SANTHOSHKUMAR-CHINNADURAI/settings`**
2. In the **Repository name** field, remove the leading hyphen `-` so the name is:  
   👉 **`santhoshkumar-chinnadurai`**
3. Click **Rename**.
4. In your terminal in this workspace folder, commit and push the new `README.md`:
   ```bash
   git add README.md
   git commit -m "feat: launch professional recruiter-ready GitHub profile README"
   git push origin main
   ```
5. Visit your GitHub profile at `https://github.com/santhoshkumar-chinnadurai`. Your custom profile banner is now active!

---

## ⚡ Step 2: Rename Key Repositories on GitHub

For each repository below, go to **GitHub > [Repository] > Settings > General > Repository Name**, rename it, and click **Rename**:

| Current Name | New Professional Name |
|---|---|
| `job-` | `job-portal-api` |
| `new-civic` | `ecocivic-issue-reporting-system` |
| `crowd-funding` | `crowdfunding-platform` |
| `portfolio` | `developer-portfolio-nextjs` |
| `E-Commerce-Web-Application` | `ecommerce-web-platform` |
| `Blog-Platform-with-Comments` | `blog-platform-api` |
| `Task-Management-Application` | `task-management-app` |
| `santhoshkumar` | `personal-portfolio-vite` |
| `new-portfolio` | `cosmic-bento-portfolio` |
| `super-market-project` | `supermarket-store-react` |

---

## ⚡ Step 3: Apply Production READMEs & .gitignore Files

All production READMEs, `.env.example`, and `.gitignore` files have been generated in the `portfolio-rebuild-kit/` directory in this workspace:

- `portfolio-rebuild-kit/job-portal-api/` ──► Copy to `job-portal-api` repo
- `portfolio-rebuild-kit/crowdfunding-platform/` ──► Copy to `crowdfunding-platform` repo
- `portfolio-rebuild-kit/ecocivic-issue-reporting-system/` ──► Copy to `ecocivic-issue-reporting-system` repo
- `portfolio-rebuild-kit/developer-portfolio-nextjs/` ──► Copy to `developer-portfolio-nextjs` repo
- `portfolio-rebuild-kit/ecommerce-web-platform/` ──► Copy to `ecommerce-web-platform` repo
- `portfolio-rebuild-kit/blog-platform-api/` ──► Copy to `blog-platform-api` repo
- `portfolio-rebuild-kit/task-management-app/` ──► Copy to `task-management-app` repo

---

## ⚡ Step 4: Archive / Make Private Weak & Duplicate Repositories

Go to **Repository > Settings > General > Danger Zone > Change repository visibility > Change to Private** for:
1. `react` *(Coursework assignments; contains exposed API key)*
2. `Malware-deduction-e` *(Academic PDF report only)*
3. `Online-Store-Inventory-Management` *(Academic PDF report & Bubble link)*
4. `Gokul-m` *(Unmodified upstream template)*
5. `crowd-funding-deploy` *(Duplicate repository)*
6. `civic-reporting-system` *(Consolidated into `ecocivic-issue-reporting-system`)*

---

## ⚡ Step 5: Pin Your Top 6 Flagship Repositories

1. Go to your main GitHub profile page: `https://github.com/santhoshkumar-chinnadurai`.
2. Scroll to the **Pinned** section and click **Customize your pins**.
3. Select these 6 repositories in order:
   - 📌 **1. `ecocivic-issue-reporting-system`** (NestJS + PostgreSQL + React 19)
   - 📌 **2. `crowdfunding-platform`** (Java 21 + Spring Boot 3 + React)
   - 📌 **3. `job-portal-api`** (Java 21 + Spring Boot 3.4 + OpenAPI)
   - 📌 **4. `developer-portfolio-nextjs`** (Next.js 16 + TypeScript + Three.js)
   - 📌 **5. `ecommerce-web-platform`** (Node.js + Express + MongoDB)
   - 📌 **6. `blog-platform-api`** (Node.js + Express + JWT Auth)
4. Click **Save pins**.
