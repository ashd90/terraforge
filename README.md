<div align="center">

<img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/terraform/terraform-original.svg" width="90" alt="Terraform logo" />

# 🔨 terraforge

**A complete, beginner-to-production Terraform learning repository**
*Structured · Project-based · Fully documented · Azure free tier*

[![Terraform](https://img.shields.io/badge/Terraform-1.7+-7B42BC?style=flat-square&logo=terraform&logoColor=white)](https://developer.hashicorp.com/terraform)
[![Azure](https://img.shields.io/badge/Cloud-Microsoft%20Azure-0078D4?style=flat-square&logo=microsoftazure&logoColor=white)](https://azure.microsoft.com)
[![License](https://img.shields.io/badge/License-MIT-green?style=flat-square)](LICENSE)
[![roadmap.sh](https://img.shields.io/badge/Follows-roadmap.sh%2Fterraform-FF5722?style=flat-square)](https://roadmap.sh/terraform)

---

*From zero to production-grade infrastructure — one section at a time.*

</div>

---

## 📖 About this repository

**terraforge** is a self-paced, hands-on Terraform learning journal built around the [roadmap.sh/terraform](https://roadmap.sh/terraform) curriculum. Every concept is explored through real cloud infrastructure on **Microsoft Azure** (free tier), progressing from the absolute basics of Infrastructure as Code all the way to production pipelines, modules, and CI/CD automation.

Each section follows a consistent rhythm:
- **Theory first** — understand the *why* before the *how*
- **3–4 guided examples** — build muscle memory with annotated code
- **One real project** — apply everything in a complete, working deployment
- **A detailed README** — your permanent reference for that topic

> This repo is both a learning environment and a living reference. Every README is written to be re-read months later.

---

## 🗂️ Repository structure
---

## 🗺️ Learning roadmap

| Phase | Topic | Projects | Status |
|-------|-------|----------|--------|
| **1** | 🏗️ Foundations — IaC, install, HCL, core workflow | Resource Group | ⬜ Not started |
| **2** | ⚙️ Core config — Variables, outputs, locals, data sources | Storage Account | ⬜ Not started |
| **3** | 💾 State management — Backends, import, state commands | Remote backend | ⬜ Not started |
| **4** | 📦 Modules — Writing, Registry, meta-arguments | Web app module | ⬜ Not started |
| **5** | 🔬 Advanced — Workspaces, functions, testing | Multi-env app | ⬜ Not started |
| **6** | 🚀 Production — CI/CD, security, Terraform Cloud | Full stack capstone | ⬜ Not started |

> Update the status column as you progress: ⬜ Not started → 🔄 In progress → ✅ Complete

---

## 🧰 Prerequisites

Before starting, make sure you have these installed and configured:

### Required tools

| Tool | Purpose | Version |
|------|---------|---------|
| [Terraform CLI](https://developer.hashicorp.com/terraform/install) | Core IaC tool | >= 1.7 |
| [Azure CLI](https://learn.microsoft.com/en-us/cli/azure/install-azure-cli-linux) | Authenticate with Azure | latest |
| [Git](https://git-scm.com/) | Version control | latest |
| [VS Code](https://code.visualstudio.com/) | Editor | latest |
| [tfenv](https://github.com/tfutils/tfenv) *(optional but recommended)* | Manage multiple Terraform versions | latest |

### Installation — Arch Linux

```bash
# ── System update (always do this first on Arch) ──────────────────────────
sudo pacman -Syu

# ── Git ───────────────────────────────────────────────────────────────────
sudo pacman -S git

# ── Terraform (via official Arch extra repository) ────────────────────────
sudo pacman -S terraform

# Verify
terraform -v

# ── OR: tfenv — manage multiple Terraform versions (recommended) ──────────
# Lets you switch versions per project via the .terraform-version file
yay -S tfenv
tfenv install 1.7.0
tfenv use 1.7.0
terraform -v

# ── Azure CLI ─────────────────────────────────────────────────────────────
# Option 1: AUR (easiest, stays up to date)
yay -S azure-cli

# Option 2: pip install (no AUR helper needed)
sudo pacman -S python-pip
pip install azure-cli --user

# Verify
az --version

# ── VS Code ───────────────────────────────────────────────────────────────
# Open-source build — official Arch repos
sudo pacman -S code

# OR: Microsoft binary with full marketplace access (AUR)
yay -S visual-studio-code-bin

# ── Install yay AUR helper if you don't have one ─────────────────────────
sudo pacman -S --needed base-devel
git clone https://aur.archlinux.org/yay.git /tmp/yay
cd /tmp/yay && makepkg -si && cd -
```

> 💡 **Arch tip:** Terraform lives in the official `extra` repository so `sudo pacman -S terraform` is the cleanest path. Use `tfenv` from the AUR only if you need to juggle multiple versions across projects.

### Recommended VS Code extensions

```bash
code --install-extension hashicorp.terraform
code --install-extension ms-azuretools.vscode-azureterraform
code --install-extension eamodio.gitlens
code --install-extension mhutchie.git-graph
```

| Extension | ID | Purpose |
|-----------|-----|---------|
| HashiCorp Terraform | `hashicorp.terraform` | Syntax highlighting, autocomplete, fmt on save |
| Azure Terraform | `ms-azuretools.vscode-azureterraform` | Azure-specific resource snippets |
| GitLens | `eamodio.gitlens` | Git blame, history, diff in editor |
| Git Graph | `mhutchie.git-graph` | Visual branch and commit graph |

### Azure account setup

```bash
# Log in to Azure (opens browser for auth)
az login

# Verify your active subscription
az account show

# List all subscriptions if you have multiple
az account list --output table

# Set a specific subscription as default
az account set --subscription "YOUR_SUBSCRIPTION_NAME_OR_ID"

# Confirm the right subscription is active
az account show --query "{name:name, id:id, state:state}" --output table
```

---

## ⚡ Quick start

```bash
# Clone the repository
git clone https://github.com/YOUR_USERNAME/terraforge.git
cd terraforge

# Verify Terraform is installed
terraform -v

# Navigate to the first section and begin
cd 01-foundations/03-core-workflow/examples/example-01-hello-azure
```

---

## 📐 How each section is structured

Every topic folder contains a `README.md` with these sections:

| Section | Contents |
|---------|----------|
| 🎯 **Overview** | What you'll learn, time estimate, Azure cost |
| 📚 **Theory** | Concept explained in plain language with diagrams |
| 💻 **Commands** | Full annotated command reference |
| 🧪 **Examples** | 3–4 step-by-step examples with full code |
| ❓ **FAQ** | Answers to the most common questions |
| 🏭 **Production use case** | How real companies use this in practice |
| 🐛 **Troubleshooting** | Common errors and exactly how to fix them |
| 🔗 **References** | Official docs and further reading |
| 📝 **Notes** | Your personal observations and aha-moments |

---

## ☁️ Cloud provider — Microsoft Azure

All projects in this repo use **Microsoft Azure** on the free tier.

### Free tier services used in this repo

| Azure service | Free allowance | Used in phase |
|--------------|---------------|---------------|
| Resource Groups | Always free | Phase 1 |
| Storage Account (Blob) | 5 GB always free | Phase 2, 3 |
| App Service | 10 free apps (F1 tier) | Phase 4 |
| Static Web Apps | Free tier, always | Phase 5 |
| Azure SQL Database | 100k vCore-sec/month free | Phase 6 |
| Key Vault | 10k operations/month free | Phase 6 |
| Virtual Networks | Always free to create | Phase 4+ |

> ⚠️ **Important:** Always run `terraform destroy` at the end of each exercise to avoid accidental charges. Every section README reminds you of this.

---

## 🔐 Security practices in this repo
---

## 📝 Git conventions

Commit messages follow this pattern:
---

## 📚 Key references

- 📘 [Terraform documentation](https://developer.hashicorp.com/terraform/docs)
- 🗺️ [roadmap.sh/terraform](https://roadmap.sh/terraform) — the curriculum this repo follows
- 🔵 [Azure Terraform provider docs](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs)
- 🧩 [Terraform Registry — modules](https://registry.terraform.io)
- 🎓 [HashiCorp Learn](https://developer.hashicorp.com/terraform/tutorials)

---

## 📄 License

MIT — feel free to fork, adapt, and build on this for your own learning.

---

<div align="center">

Built with patience, one `terraform apply` at a time. 🔨

</div>
