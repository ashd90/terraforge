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

**terraforge** is a self-paced, hands-on Terraform learning journal built around the
[roadmap.sh/terraform](https://roadmap.sh/terraform) curriculum. Every concept is explored
through real cloud infrastructure on **Microsoft Azure** (free tier), progressing from the
absolute basics of Infrastructure as Code all the way to production pipelines, modules,
and CI/CD automation.

Each section follows a consistent rhythm:

- **Theory first** — concepts explained with real-world analogies, no diagrams
- **10 guided examples** — deep practice building muscle memory with annotated code
- **One real project** — apply everything in a complete, working deployment
- **A detailed README** — your permanent reference, written to be re-read months later

---

## 🗂️ Repository structure

    ~/repoHive/terraforge/
    │
    ├── 📁 01-foundations/
    │   ├── README.md
    │   ├── 01-iac-concepts/
    │   ├── 02-install-and-setup/
    │   ├── 03-core-workflow/
    │   │   └── project-01-resource-group/     ← 🚀 Project 1
    │   ├── 04-hcl-basics/
    │   └── 05-providers/
    │
    ├── 📁 02-core-config/
    │   ├── README.md
    │   ├── 01-variables/
    │   ├── 02-outputs/
    │   ├── 03-locals/
    │   ├── 04-data-sources/
    │   ├── 05-expressions-and-functions/
    │   ├── 06-meta-arguments/
    │   ├── 07-dynamic-blocks/
    │   ├── 08-dependency-graph/
    │   └── project-02-storage-account/        ← 🚀 Project 2
    │
    ├── 📁 03-state-management/
    │   ├── README.md
    │   ├── 01-state-internals/
    │   ├── 02-remote-backends/
    │   ├── 03-state-commands/
    │   ├── 04-import/
    │   ├── 05-moved-blocks/
    │   ├── 06-state-locking/
    │   └── project-03-remote-state/           ← 🚀 Project 3
    │
    ├── 📁 04-modules/
    │   ├── README.md
    │   ├── 01-module-basics/
    │   ├── 02-writing-modules/
    │   ├── 03-module-composition/
    │   ├── 04-registry-modules/
    │   ├── 05-module-versioning/
    │   ├── 06-meta-arguments-in-modules/
    │   ├── modules/                            ← reusable module library
    │   │   ├── azure-resource-group/
    │   │   ├── azure-storage-account/
    │   │   ├── azure-virtual-network/
    │   │   └── azure-app-service/
    │   └── project-04-webapp-module/           ← 🚀 Project 4
    │
    ├── 📁 05-advanced/
    │   ├── README.md
    │   ├── 01-workspaces/
    │   ├── 02-built-in-functions/
    │   ├── 03-provisioners/
    │   ├── 04-null-resource/
    │   ├── 05-terraform-console/
    │   ├── 06-check-blocks/
    │   ├── 07-testing/
    │   └── project-05-multi-env/               ← 🚀 Project 5
    │
    ├── 📁 06-production/
    │   ├── README.md
    │   ├── 01-best-practices/
    │   ├── 02-security/
    │   ├── 03-environment-variables/
    │   ├── 04-cicd-github-actions/
    │   │   └── .github/workflows/
    │   ├── 05-terraform-cloud/
    │   ├── 06-policy-as-code/
    │   ├── 07-drift-detection/
    │   └── project-06-capstone/                ← 🏆 Project 6
    │
    ├── 📄 .gitignore
    ├── 📄 .terraform-version
    └── 📄 CONVENTIONS.md

---

## 🗺️ Learning roadmap

| # | Phase | Topics | Project | Status |
|---|-------|--------|---------|--------|
| 1 | 🏗️ Foundations | IaC concepts, install, core workflow, HCL, providers | Resource Group | ⬜ Not started |
| 2 | ⚙️ Core config | Variables, outputs, locals, data sources, functions, meta-args, dynamic blocks, dependency graph | Storage Account | ⬜ Not started |
| 3 | 💾 State management | Internals, backends, state commands, import, moved blocks, locking | Remote backend | ⬜ Not started |
| 4 | 📦 Modules | Basics, writing, composition, registry, versioning, meta-args | Web app module | ⬜ Not started |
| 5 | 🔬 Advanced | Workspaces, functions, provisioners, null resource, console, check blocks, testing | Multi-env app | ⬜ Not started |
| 6 | 🚀 Production | Best practices, security, env vars, CI/CD, TF Cloud, policy as code, drift detection | Full stack capstone | ⬜ Not started |

> Update status as you go: ⬜ Not started → 🔄 In progress → ✅ Complete

---

## 🧰 Prerequisites

### Required tools

| Tool | Purpose | Version |
|------|---------|---------|
| [Terraform CLI](https://developer.hashicorp.com/terraform/install) | Core IaC tool | >= 1.7 |
| [Azure CLI](https://learn.microsoft.com/en-us/cli/azure/install-azure-cli-linux) | Authenticate with Azure | latest |
| [Git](https://git-scm.com/) | Version control | latest |
| [VS Code](https://code.visualstudio.com/) | Editor | latest |
| [tfenv](https://github.com/tfutils/tfenv) *(recommended)* | Manage multiple Terraform versions | latest |

### Installation — Arch Linux

```bash
# ── System update ────────────────────────────────────────────────────────
sudo pacman -Syu

# ── Git ──────────────────────────────────────────────────────────────────
sudo pacman -S git

# ── Terraform (official Arch extra repository) ───────────────────────────
sudo pacman -S terraform
terraform -v

# ── OR: tfenv for version management (recommended) ───────────────────────
yay -S tfenv
tfenv install 1.7.0
tfenv use 1.7.0
terraform -v

# ── Azure CLI ────────────────────────────────────────────────────────────
yay -S azure-cli
az --version

# ── VS Code ──────────────────────────────────────────────────────────────
sudo pacman -S code
# OR Microsoft binary with full marketplace:
yay -S visual-studio-code-bin

# ── Install yay AUR helper if needed ─────────────────────────────────────
sudo pacman -S --needed base-devel
git clone https://aur.archlinux.org/yay.git /tmp/yay
cd /tmp/yay && makepkg -si && cd -
```

> 💡 **Arch tip:** Terraform is in the `extra` repository. Use `tfenv` from AUR only if you need version switching between projects.

### Recommended VS Code extensions

```bash
code --install-extension hashicorp.terraform
code --install-extension ms-azuretools.vscode-azureterraform
code --install-extension eamodio.gitlens
code --install-extension mhutchie.git-graph
```

### Azure account setup

```bash
az login
az account show
az account list --output table
az account set --subscription "YOUR_SUBSCRIPTION_NAME_OR_ID"
az account show --query "{name:name, id:id, state:state}" --output table
```

---

## ⚡ Quick start

```bash
git clone https://github.com/YOUR_USERNAME/terraforge.git ~/repoHive/terraforge
cd ~/repoHive/terraforge
terraform -v
cd 01-foundations/03-core-workflow/examples/example-01-first-resource-group
```

---

## 📐 How each section is structured

Every topic folder contains a README.md with these sections:

| Section | Contents |
|---------|----------|
| 🎯 **Overview** | What you will learn, time estimate, Azure cost |
| 📚 **Theory** | Concepts explained with real-world analogies |
| 💻 **Commands** | Full annotated command reference |
| 🧪 **Examples** | 10 step-by-step examples with full annotated code |
| ❓ **FAQ** | Answers to the most common questions |
| 🏭 **Production use case** | How real companies use this in practice |
| 🐛 **Troubleshooting** | Common errors and exactly how to fix them |
| 🔗 **References** | Official docs and further reading |
| 📝 **Notes** | Your personal observations and aha-moments |

---

## ☁️ Cloud provider — Microsoft Azure (free tier)

| Azure service | Free allowance | Phase |
|--------------|---------------|-------|
| Resource Groups | Always free | 1 |
| Storage Account (Blob) | 5 GB always free | 2, 3 |
| App Service (F1) | 10 free apps | 4 |
| Static Web Apps | Free tier, always | 5 |
| Azure SQL Database | 100k vCore-sec/month | 6 |
| Key Vault | 10k operations/month | 6 |
| Virtual Networks | Always free | 4+ |

> ⚠️ Always run `terraform destroy` after every exercise to avoid charges.

---

## 🔐 Security practices

    ✅  .tfstate files are gitignored — never committed
    ✅  .tfvars files are gitignored — only .tfvars.example is committed
    ✅  .terraform/ directory is gitignored
    ✅  Secrets use environment variables or Azure Key Vault, never hardcoded
    ✅  Service principal credentials stored in GitHub Secrets (Phase 6)

---

## 📝 Git conventions

    feat(phase1):    Add example-01 first resource group
    feat(phase2):    Complete project-02 storage account
    docs(phase1):    Add README for core-workflow section
    fix(phase3):     Correct backend config in remote-state project
    chore:           Update .gitignore

---

## 📚 Key references

- 📘 [Terraform documentation](https://developer.hashicorp.com/terraform/docs)
- 🗺️ [roadmap.sh/terraform](https://roadmap.sh/terraform)
- 🔵 [Azure Provider docs](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs)
- 🧩 [Terraform Registry](https://registry.terraform.io)
- 🎓 [HashiCorp Learn](https://developer.hashicorp.com/terraform/tutorials)

---

## 📄 License

MIT — feel free to fork, adapt, and build on this for your own learning.

---

<div align="center">

Built with patience, one `terraform apply` at a time. 🔨

</div>
