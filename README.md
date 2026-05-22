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

```
terraforge/
│
├── 📁 01-foundations/              # Phase 1 — IaC concepts, setup, HCL, core workflow
│   ├── 01-iac-concepts/            #   What is IaC? Why Terraform?
│   ├── 02-install-and-setup/       #   Terraform CLI + Azure CLI + provider auth
│   ├── 03-core-workflow/           #   init → plan → apply → destroy
│   │   ├── examples/               #   3 guided examples
│   │   └── project-01-resource-group/  ← 🚀 First real project
│   └── 04-hcl-basics/              #   Blocks, arguments, expressions, types
│
├── 📁 02-core-config/              # Phase 2 — Variables, outputs, locals, data sources
│   ├── 01-variables/
│   ├── 02-outputs/
│   ├── 03-locals/
│   ├── 04-data-sources/
│   ├── 05-dependency-graph/
│   └── project-02-storage-account/    ← 🚀 Azure Storage Account
│
├── 📁 03-state-management/         # Phase 3 — State internals, remote backends, import
│   ├── 01-state-internals/
│   ├── 02-remote-backends/
│   ├── 03-state-commands/
│   ├── 04-import/
│   └── project-03-remote-state/        ← 🚀 Azure Blob remote backend
│
├── 📁 04-modules/                  # Phase 4 — Modules, Registry, meta-arguments
│   ├── 01-module-basics/
│   ├── 02-writing-modules/
│   ├── 03-registry-modules/
│   ├── 04-meta-arguments/
│   ├── modules/                    #   Reusable modules library
│   │   ├── azure-resource-group/
│   │   ├── azure-storage-account/
│   │   └── azure-app-service/
│   └── project-04-webapp-module/       ← 🚀 Azure App Service via module
│
├── 📁 05-advanced/                 # Phase 5 — Workspaces, functions, provisioners, testing
│   ├── 01-workspaces/
│   ├── 02-functions/
│   ├── 03-provisioners/
│   ├── 04-testing/
│   └── project-05-multi-env/           ← 🚀 Dev/prod workspace setup
│
├── 📁 06-production/               # Phase 6 — Best practices, security, CI/CD, Terraform Cloud
│   ├── 01-best-practices/
│   ├── 02-security/
│   ├── 03-cicd-github-actions/
│   ├── 04-terraform-cloud/
│   └── project-06-capstone/            ← 🏆 Full Azure stack + GitHub Actions pipeline
│
├── 📄 .gitignore                   # Excludes .tfstate, .terraform/, secrets
├── 📄 .terraform-version           # Pins Terraform version via tfenv
└── 📄 CONVENTIONS.md               # Naming rules, tagging policy, git workflow
```

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

| Tool | Purpose | Install |
|------|---------|---------|
| [Terraform CLI](https://developer.hashicorp.com/terraform/install) `≥ 1.7` | Core IaC tool | `brew install terraform` / [direct download](https://developer.hashicorp.com/terraform/install) |
| [Azure CLI](https://learn.microsoft.com/en-us/cli/azure/install-azure-cli) | Authenticate with Azure | `brew install azure-cli` |
| [Git](https://git-scm.com/) | Version control | `brew install git` |
| [VS Code](https://code.visualstudio.com/) | Editor | + HashiCorp Terraform extension |

### Recommended VS Code extensions

```
HashiCorp Terraform       (hashicorp.terraform)
Azure Terraform           (ms-azuretools.vscode-azureterraform)
GitLens                   (eamodio.gitlens)
```

### Azure account setup

```bash
# Log in to Azure
az login

# Verify your subscription is active
az account show

# Set a default subscription (if you have multiple)
az account set --subscription "YOUR_SUBSCRIPTION_NAME"
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

# Follow the README.md inside that folder
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

> ⚠️ **Important:** Always run `terraform destroy` at the end of each exercise to avoid any accidental charges. Every section README reminds you of this.

---

## 🔐 Security practices in this repo

```
✅  .tfstate files are gitignored — never committed
✅  .tfvars files are gitignored — only .tfvars.example is committed
✅  .terraform/ directory is gitignored
✅  Secrets use environment variables or Azure Key Vault, never hardcoded
✅  Service principal credentials are stored in GitHub Secrets (Phase 6)
```

---

## 📝 Git conventions

Commit messages follow this pattern:

```
feat(phase1):    Add example-01 hello azure
feat(phase2):    Complete project-02 storage account
docs(phase1):    Fill in README for core-workflow section
fix(phase3):     Correct backend config in remote-state project
chore:           Update .gitignore for crash logs
```

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
