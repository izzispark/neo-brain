# izzi Spark - Company Overview

## Company
- **Name:** izzi Spark
- **Website:** (to be documented)
- **Founded:** (to be documented)
- **Industry:** (to be documented)

## Founder
- **Name:** Josafá
- **Email:** josafa.porto@gmail.com
- **Role:** Founder / CEO

## CTO Context
Neo reports directly to Josafá. All technical decisions are made in alignment with Josafá's business vision.

## Infrastructure
- **Hosting:** Hostinger KVM4 plan
- **Control Panel:** Dokploy v0.29.5 (https://host.izzispark.cloud)
- **GitHub Org:** izzispark (repos: neo-brain, website, etc.)

## Current Projects

### 1. Coder (Development Environment)
- **Type:** Docker Compose
- **URL:** (to be documented)
- **Version:** v2.15.3
- **Status:** Running (12h+ uptime)
- **Stack:** Coder + PostgreSQL 17
- **Project ID:** OpvD7JOXnNYzf1c_ULEgT
- **Service:** dev-env-coder (compose)
- **Containers:** coder-1 (running), db-1 (healthy)

### 2. Website (Frontend)
- **Type:** Application (GitHub deploy)
- **Repo:** izzi-spark-website
- **Branch:** main
- **Provider:** GitHub (izzi Spark Dokploy)
- **Webhook:** https://host.izzispark.cloud/api/deploy/2WRwQ_UHZiVSfTRrxC432
- **Build:** Dockerfile
- **Status:** ⚠️ Deploys failing (Azure/Bun pipeline issues)

## Tech Stack
- **Infra:** Docker + Dokploy (self-hosted)
- **CI/CD:** GitHub Actions
- **Database:** PostgreSQL 17
- **Development:** Coder (remote dev environments)
- **Frontend:** (to be documented)

## Known Issues
1. Website frontend deployments failing - Azure Static Web Apps workflow with Bun causing build errors on Dokploy

## Created
2026-05-23