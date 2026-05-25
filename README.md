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

- **Theory first** — understand the *why* before the *how*, explained with real-world analogies
- **9–10 guided examples** — deep practice building muscle memory with annotated code
- **One real project** — apply everything in a complete, working deployment
- **A detailed README** — your permanent reference for that topic, written to be re-read months later

---

## 🗂️ Repository structure

    ~/repoHive/terraforge/
    │
    ├── 📁 01-foundations/
    │   ├── README.md                          # Phase overview + learning objectives
    │   ├── 01-iac-concepts/
    │   │   └── README.md                      # Theory: IaC, Terraform vs others, analogies
    │   ├── 02-install-and-setup/
    │   │   ├── README.md                      # Install steps, Azure CLI auth, troubleshooting
    │   │   └── verify.tf                      # Provider block to confirm setup works
    │   ├── 03-core-workflow/
    │   │   ├── README.md                      # init → plan → apply → destroy deep dive
    │   │   ├── examples/
    │   │   │   ├── example-01-first-resource-group/
    │   │   │   ├── example-02-provider-version-constraints/
    │   │   │   ├── example-03-reading-plan-output/
    │   │   │   ├── example-04-plan-with-output-file/
    │   │   │   ├── example-05-auto-approve/
    │   │   │   ├── example-06-targeted-apply/
    │   │   │   ├── example-07-terraform-fmt/
    │   │   │   ├── example-08-terraform-validate/
    │   │   │   ├── example-09-multiple-resources/
    │   │   │   └── example-10-destroy-targeted/
    │   │   └── project-01-resource-group/     # 🚀 First real project
    │   ├── 04-hcl-basics/
    │   │   ├── README.md                      # Blocks, arguments, expressions, types
    │   │   └── examples/
    │   │       ├── example-01-block-types/
    │   │       ├── example-02-argument-types/
    │   │       ├── example-03-string-types/
    │   │       ├── example-04-number-and-bool/
    │   │       ├── example-05-list-type/
    │   │       ├── example-06-map-type/
    │   │       ├── example-07-object-type/
    │   │       ├── example-08-tuple-type/
    │   │       ├── example-09-type-conversion/
    │   │       └── example-10-comments-and-style/
    │   └── 05-providers/
    │       ├── README.md                      # Provider blocks, registry, auth, aliases
    │       └── examples/
    │           ├── example-01-basic-provider/
    │           ├── example-02-version-constraints/
    │           ├── example-03-provider-config-options/
    │           ├── example-04-required-providers-block/
    │           ├── example-05-lock-file/
    │           ├── example-06-provider-upgrade/
    │           ├── example-07-multiple-providers/
    │           ├── example-08-provider-alias/
    │           ├── example-09-provider-env-vars/
    │           └── example-10-provider-meta-argument/
    │
    ├── 📁 02-core-config/
    │   ├── README.md
    │   ├── 01-variables/
    │   │   ├── README.md                      # Input vars, types, validation, sensitive, tfvars
    │   │   └── examples/
    │   │       ├── example-01-basic-variable/
    │   │       ├── example-02-variable-types/
    │   │       ├── example-03-default-values/
    │   │       ├── example-04-validation-rules/
    │   │       ├── example-05-sensitive-variable/
    │   │       ├── example-06-tfvars-file/
    │   │       ├── example-07-cli-var-flag/
    │   │       ├── example-08-environment-variable/
    │   │       ├── example-09-complex-variable-types/
    │   │       └── example-10-variable-precedence/
    │   ├── 02-outputs/
    │   │   ├── README.md
    │   │   └── examples/
    │   │       ├── example-01-basic-output/
    │   │       ├── example-02-output-expressions/
    │   │       ├── example-03-sensitive-output/
    │   │       ├── example-04-output-from-resource/
    │   │       ├── example-05-multiple-outputs/
    │   │       ├── example-06-output-list/
    │   │       ├── example-07-output-map/
    │   │       ├── example-08-conditional-output/
    │   │       ├── example-09-output-depends-on/
    │   │       └── example-10-cross-module-output/
    │   ├── 03-locals/
    │   │   ├── README.md
    │   │   └── examples/
    │   │       ├── example-01-basic-local/
    │   │       ├── example-02-local-from-variable/
    │   │       ├── example-03-local-string-concat/
    │   │       ├── example-04-local-map/
    │   │       ├── example-05-local-list/
    │   │       ├── example-06-local-conditional/
    │   │       ├── example-07-local-from-data-source/
    │   │       ├── example-08-local-computed-tags/
    │   │       ├── example-09-local-naming-convention/
    │   │       └── example-10-locals-best-practices/
    │   ├── 04-data-sources/
    │   │   ├── README.md
    │   │   └── examples/
    │   │       ├── example-01-basic-data-source/
    │   │       ├── example-02-azure-subscription-data/
    │   │       ├── example-03-existing-resource-group/
    │   │       ├── example-04-data-source-filters/
    │   │       ├── example-05-data-into-resource/
    │   │       ├── example-06-multiple-data-sources/
    │   │       ├── example-07-data-source-depends-on/
    │   │       ├── example-08-resource-vs-data/
    │   │       ├── example-09-data-for-policy/
    │   │       └── example-10-data-in-modules/
    │   ├── 05-expressions-and-functions/
    │   │   ├── README.md                      # All function categories + terraform console
    │   │   └── examples/
    │   │       ├── example-01-string-functions/
    │   │       ├── example-02-numeric-functions/
    │   │       ├── example-03-collection-functions/
    │   │       ├── example-04-type-functions/
    │   │       ├── example-05-filesystem-functions/
    │   │       ├── example-06-encoding-functions/
    │   │       ├── example-07-date-time-functions/
    │   │       ├── example-08-templatefile-function/
    │   │       ├── example-09-conditional-expressions/
    │   │       └── example-10-for-expressions/
    │   ├── 06-meta-arguments/
    │   │   ├── README.md                      # depends_on, lifecycle, count, for_each, provider
    │   │   └── examples/
    │   │       ├── example-01-depends-on/
    │   │       ├── example-02-count/
    │   │       ├── example-03-for-each-list/
    │   │       ├── example-04-for-each-map/
    │   │       ├── example-05-lifecycle-create-before-destroy/
    │   │       ├── example-06-lifecycle-prevent-destroy/
    │   │       ├── example-07-lifecycle-ignore-changes/
    │   │       ├── example-08-lifecycle-replace-triggered-by/
    │   │       ├── example-09-provider-meta-argument/
    │   │       └── example-10-combined-meta-arguments/
    │   ├── 07-dynamic-blocks/
    │   │   ├── README.md
    │   │   └── examples/
    │   │       ├── example-01-basic-dynamic-block/
    │   │       ├── example-02-dynamic-with-for-each/
    │   │       ├── example-03-dynamic-iterator/
    │   │       ├── example-04-nested-dynamic/
    │   │       ├── example-05-dynamic-in-resource/
    │   │       ├── example-06-dynamic-from-variable/
    │   │       ├── example-07-dynamic-conditional/
    │   │       ├── example-08-dynamic-security-rules/
    │   │       ├── example-09-dynamic-tags/
    │   │       └── example-10-dynamic-best-practices/
    │   ├── 08-dependency-graph/
    │   │   ├── README.md
    │   │   └── examples/
    │   │       ├── example-01-implicit-dependency/
    │   │       ├── example-02-explicit-depends-on/
    │   │       ├── example-03-dependency-chain/
    │   │       ├── example-04-parallel-resources/
    │   │       ├── example-05-terraform-graph-command/
    │   │       ├── example-06-circular-dependency-fix/
    │   │       ├── example-07-data-source-dependency/
    │   │       ├── example-08-module-dependency/
    │   │       ├── example-09-cross-module-dependency/
    │   │       └── example-10-dependency-real-world/
    │   └── project-02-storage-account/        # 🚀 Azure Storage Account
    │
    ├── 📁 03-state-management/
    │   ├── README.md
    │   ├── 01-state-internals/
    │   │   ├── README.md                      # tfstate format, what's inside, drift
    │   │   └── examples/
    │   │       ├── example-01-inspect-local-state/
    │   │       ├── example-02-state-after-apply/
    │   │       ├── example-03-state-after-change/
    │   │       ├── example-04-state-after-destroy/
    │   │       ├── example-05-terraform-show/
    │   │       ├── example-06-manual-drift-simulation/
    │   │       ├── example-07-terraform-refresh/
    │   │       ├── example-08-state-serial-number/
    │   │       ├── example-09-sensitive-data-in-state/
    │   │       └── example-10-state-format-deep-dive/
    │   ├── 02-remote-backends/
    │   │   ├── README.md                      # Local vs remote, Azure Blob, state locking
    │   │   └── examples/
    │   │       ├── example-01-local-backend/
    │   │       ├── example-02-azurerm-backend-config/
    │   │       ├── example-03-backend-init/
    │   │       ├── example-04-backend-migration/
    │   │       ├── example-05-partial-backend-config/
    │   │       ├── example-06-backend-with-vars/
    │   │       ├── example-07-multiple-envs-one-backend/
    │   │       ├── example-08-backend-reconfigure/
    │   │       ├── example-09-backend-state-encryption/
    │   │       └── example-10-backend-best-practices/
    │   ├── 03-state-commands/
    │   │   ├── README.md                      # list, show, mv, rm, pull, push, force-unlock
    │   │   └── examples/
    │   │       ├── example-01-state-list/
    │   │       ├── example-02-state-show/
    │   │       ├── example-03-state-mv-rename/
    │   │       ├── example-04-state-mv-to-module/
    │   │       ├── example-05-state-rm/
    │   │       ├── example-06-state-pull/
    │   │       ├── example-07-state-push/
    │   │       ├── example-08-force-unlock/
    │   │       ├── example-09-state-replace-provider/
    │   │       └── example-10-state-operations-workflow/
    │   ├── 04-import/
    │   │   ├── README.md                      # CLI import, import blocks (1.5+), workflow
    │   │   └── examples/
    │   │       ├── example-01-basic-cli-import/
    │   │       ├── example-02-import-resource-group/
    │   │       ├── example-03-import-storage-account/
    │   │       ├── example-04-import-block-syntax/
    │   │       ├── example-05-import-with-for-each/
    │   │       ├── example-06-import-into-module/
    │   │       ├── example-07-generate-config-after-import/
    │   │       ├── example-08-import-complex-resource/
    │   │       ├── example-09-import-drift-fix/
    │   │       └── example-10-import-full-workflow/
    │   ├── 05-moved-blocks/
    │   │   ├── README.md                      # Declarative refactoring, no destroy needed
    │   │   └── examples/
    │   │       ├── example-01-rename-resource/
    │   │       ├── example-02-move-into-module/
    │   │       ├── example-03-move-between-modules/
    │   │       ├── example-04-move-with-for-each/
    │   │       ├── example-05-move-vs-state-mv/
    │   │       ├── example-06-multiple-moves/
    │   │       ├── example-07-move-and-refactor/
    │   │       ├── example-08-move-module-to-module/
    │   │       ├── example-09-removed-block/
    │   │       └── example-10-moved-in-production/
    │   ├── 06-state-locking/
    │   │   ├── README.md                      # How locking works, backends that support it
    │   │   └── examples/
    │   │       ├── example-01-lock-with-azblob/
    │   │       ├── example-02-simulate-lock-conflict/
    │   │       ├── example-03-force-unlock/
    │   │       ├── example-04-lock-timeout-flag/
    │   │       ├── example-05-lock-in-ci/
    │   │       ├── example-06-lock-disable-flag/
    │   │       ├── example-07-lock-and-teams/
    │   │       ├── example-08-lock-with-terraform-cloud/
    │   │       ├── example-09-lock-troubleshooting/
    │   │       └── example-10-lock-best-practices/
    │   └── project-03-remote-state/           # 🚀 Azure Blob remote backend + locking
    │
    ├── 📁 04-modules/
    │   ├── README.md
    │   ├── 01-module-basics/
    │   │   ├── README.md                      # Root vs child, file structure, calling syntax
    │   │   └── examples/
    │   │       ├── example-01-first-module-call/
    │   │       ├── example-02-module-with-inputs/
    │   │       ├── example-03-module-with-outputs/
    │   │       ├── example-04-module-file-structure/
    │   │       ├── example-05-local-module-path/
    │   │       ├── example-06-multiple-module-instances/
    │   │       ├── example-07-module-variable-defaults/
    │   │       ├── example-08-module-output-chaining/
    │   │       ├── example-09-module-with-providers/
    │   │       └── example-10-module-documentation/
    │   ├── 02-writing-modules/
    │   │   ├── README.md                      # Design principles, input contracts, README
    │   │   └── examples/
    │   │       ├── example-01-minimal-module/
    │   │       ├── example-02-module-variables-tf/
    │   │       ├── example-03-module-outputs-tf/
    │   │       ├── example-04-module-with-locals/
    │   │       ├── example-05-module-with-validation/
    │   │       ├── example-06-module-with-optional-vars/
    │   │       ├── example-07-module-for-each/
    │   │       ├── example-08-module-with-data-source/
    │   │       ├── example-09-module-readme-standard/
    │   │       └── example-10-module-complete/
    │   ├── 03-module-composition/
    │   │   ├── README.md                      # Modules calling modules, layered architecture
    │   │   └── examples/
    │   │       ├── example-01-nested-modules/
    │   │       ├── example-02-networking-module/
    │   │       ├── example-03-app-module-uses-network/
    │   │       ├── example-04-three-layer-composition/
    │   │       ├── example-05-output-passing-between-modules/
    │   │       ├── example-06-shared-module-pattern/
    │   │       ├── example-07-environment-composition/
    │   │       ├── example-08-dependency-between-modules/
    │   │       ├── example-09-avoiding-circular-deps/
    │   │       └── example-10-real-world-composition/
    │   ├── 04-registry-modules/
    │   │   ├── README.md                      # Finding, using, evaluating public modules
    │   │   └── examples/
    │   │       ├── example-01-using-registry-module/
    │   │       ├── example-02-registry-module-inputs/
    │   │       ├── example-03-registry-module-outputs/
    │   │       ├── example-04-module-version-pinning/
    │   │       ├── example-05-azure-registry-modules/
    │   │       ├── example-06-evaluate-module-quality/
    │   │       ├── example-07-fork-and-customise/
    │   │       ├── example-08-private-registry/
    │   │       ├── example-09-combine-registry-and-local/
    │   │       └── example-10-registry-best-practices/
    │   ├── 05-module-versioning/
    │   │   ├── README.md                      # Version constraints, lock file, upgrading
    │   │   └── examples/
    │   │       ├── example-01-exact-version/
    │   │       ├── example-02-pessimistic-constraint/
    │   │       ├── example-03-range-constraint/
    │   │       ├── example-04-latest-within-major/
    │   │       ├── example-05-lock-file-deep-dive/
    │   │       ├── example-06-terraform-init-upgrade/
    │   │       ├── example-07-version-in-git-source/
    │   │       ├── example-08-semantic-versioning/
    │   │       ├── example-09-breaking-change-handling/
    │   │       └── example-10-versioning-in-teams/
    │   ├── 06-meta-arguments-in-modules/
    │   │   ├── README.md                      # count, for_each, depends_on at module level
    │   │   └── examples/
    │   │       ├── example-01-module-count/
    │   │       ├── example-02-module-for-each/
    │   │       ├── example-03-module-for-each-map/
    │   │       ├── example-04-module-depends-on/
    │   │       ├── example-05-module-providers/
    │   │       ├── example-06-conditional-module/
    │   │       ├── example-07-module-count-vs-for-each/
    │   │       ├── example-08-module-lifecycle/
    │   │       ├── example-09-multi-region-module/
    │   │       └── example-10-meta-args-best-practices/
    │   ├── modules/                           # Reusable module library built during this phase
    │   │   ├── azure-resource-group/
    │   │   ├── azure-storage-account/
    │   │   ├── azure-virtual-network/
    │   │   └── azure-app-service/
    │   └── project-04-webapp-module/          # 🚀 Azure App Service via custom module
    │
    ├── 📁 05-advanced/
    │   ├── README.md
    │   ├── 01-workspaces/
    │   │   ├── README.md                      # Workspace isolation, use cases, limits
    │   │   └── examples/
    │   │       ├── example-01-create-workspace/
    │   │       ├── example-02-switch-workspace/
    │   │       ├── example-03-workspace-in-config/
    │   │       ├── example-04-workspace-specific-vars/
    │   │       ├── example-05-workspace-state-isolation/
    │   │       ├── example-06-workspace-list-show/
    │   │       ├── example-07-workspace-vs-separate-state/
    │   │       ├── example-08-workspace-delete/
    │   │       ├── example-09-workspace-in-ci/
    │   │       └── example-10-workspace-best-practices/
    │   ├── 02-built-in-functions/
    │   │   ├── README.md
    │   │   └── examples/
    │   │       ├── example-01-string-functions/
    │   │       ├── example-02-collection-functions/
    │   │       ├── example-03-numeric-functions/
    │   │       ├── example-04-type-functions/
    │   │       ├── example-05-encoding-functions/
    │   │       ├── example-06-filesystem-functions/
    │   │       ├── example-07-date-time-functions/
    │   │       ├── example-08-cidr-functions/
    │   │       ├── example-09-regex-functions/
    │   │       └── example-10-functions-combined/
    │   ├── 03-provisioners/
    │   │   ├── README.md                      # local-exec, remote-exec, when to avoid
    │   │   └── examples/
    │   │       ├── example-01-local-exec-basic/
    │   │       ├── example-02-local-exec-on-destroy/
    │   │       ├── example-03-remote-exec-basic/
    │   │       ├── example-04-file-provisioner/
    │   │       ├── example-05-provisioner-connection/
    │   │       ├── example-06-provisioner-on-failure/
    │   │       ├── example-07-provisioner-with-triggers/
    │   │       ├── example-08-provisioner-env-vars/
    │   │       ├── example-09-when-not-to-use/
    │   │       └── example-10-provisioner-alternatives/
    │   ├── 04-null-resource/
    │   │   ├── README.md                      # null_resource, terraform_data, triggers
    │   │   └── examples/
    │   │       ├── example-01-null-resource-basic/
    │   │       ├── example-02-null-resource-triggers/
    │   │       ├── example-03-null-resource-depends-on/
    │   │       ├── example-04-terraform-data-basic/
    │   │       ├── example-05-terraform-data-triggers/
    │   │       ├── example-06-null-vs-terraform-data/
    │   │       ├── example-07-null-for-scripts/
    │   │       ├── example-08-null-for-ordering/
    │   │       ├── example-09-null-resource-lifecycle/
    │   │       └── example-10-real-world-null-use/
    │   ├── 05-terraform-console/
    │   │   ├── README.md                      # Interactive expression testing and debugging
    │   │   └── examples/
    │   │       ├── example-01-basic-expressions/
    │   │       ├── example-02-test-string-functions/
    │   │       ├── example-03-test-collection-functions/
    │   │       ├── example-04-test-conditionals/
    │   │       ├── example-05-test-for-expressions/
    │   │       ├── example-06-inspect-state/
    │   │       ├── example-07-debug-complex-expressions/
    │   │       ├── example-08-test-templatefile/
    │   │       ├── example-09-console-in-workflow/
    │   │       └── example-10-console-best-practices/
    │   ├── 06-check-blocks/
    │   │   ├── README.md                      # Terraform 1.5+ assertions and health checks
    │   │   └── examples/
    │   │       ├── example-01-basic-check-block/
    │   │       ├── example-02-check-with-data-source/
    │   │       ├── example-03-check-http-endpoint/
    │   │       ├── example-04-check-vs-precondition/
    │   │       ├── example-05-check-vs-postcondition/
    │   │       ├── example-06-precondition-on-var/
    │   │       ├── example-07-postcondition-on-resource/
    │   │       ├── example-08-custom-error-messages/
    │   │       ├── example-09-check-in-modules/
    │   │       └── example-10-checks-in-production/
    │   ├── 07-testing/
    │   │   ├── README.md                      # validate, fmt, plan, terraform test, checkov
    │   │   └── examples/
    │   │       ├── example-01-terraform-validate/
    │   │       ├── example-02-terraform-fmt-check/
    │   │       ├── example-03-terraform-test-basic/
    │   │       ├── example-04-test-with-mocked-providers/
    │   │       ├── example-05-test-module/
    │   │       ├── example-06-checkov-scan/
    │   │       ├── example-07-tflint/
    │   │       ├── example-08-test-in-ci/
    │   │       ├── example-09-terratest-intro/
    │   │       └── example-10-full-test-pipeline/
    │   └── project-05-multi-env/              # 🚀 Dev/prod workspaces + Static Web App
    │
    ├── 📁 06-production/
    │   ├── README.md
    │   ├── 01-best-practices/
    │   │   ├── README.md                      # Project structure, naming, tagging, .gitignore
    │   │   └── examples/
    │   │       ├── example-01-file-naming/
    │   │       ├── example-02-resource-naming/
    │   │       ├── example-03-tagging-strategy/
    │   │       ├── example-04-folder-structure/
    │   │       ├── example-05-gitignore-rules/
    │   │       ├── example-06-tfvars-patterns/
    │   │       ├── example-07-version-pinning/
    │   │       ├── example-08-large-repo-layout/
    │   │       ├── example-09-documentation-standard/
    │   │       └── example-10-code-review-checklist/
    │   ├── 02-security/
    │   │   ├── README.md                      # Sensitive vars, Key Vault, least privilege
    │   │   └── examples/
    │   │       ├── example-01-sensitive-variables/
    │   │       ├── example-02-avoid-secrets-in-state/
    │   │       ├── example-03-azure-key-vault-integration/
    │   │       ├── example-04-service-principal-setup/
    │   │       ├── example-05-least-privilege-role/
    │   │       ├── example-06-environment-var-secrets/
    │   │       ├── example-07-checkov-security-scan/
    │   │       ├── example-08-state-encryption/
    │   │       ├── example-09-audit-logging/
    │   │       └── example-10-security-checklist/
    │   ├── 03-environment-variables/
    │   │   ├── README.md                      # TF_VAR_, TF_LOG, TF_CLI_ARGS, TF_DATA_DIR
    │   │   └── examples/
    │   │       ├── example-01-TF_VAR-prefix/
    │   │       ├── example-02-TF_LOG-levels/
    │   │       ├── example-03-TF_LOG-to-file/
    │   │       ├── example-04-TF_CLI_ARGS/
    │   │       ├── example-05-TF_DATA_DIR/
    │   │       ├── example-06-TF_WORKSPACE/
    │   │       ├── example-07-env-vars-in-ci/
    │   │       ├── example-08-ARM-env-vars-azure/
    │   │       ├── example-09-env-vars-security/
    │   │       └── example-10-env-vars-reference/
    │   ├── 04-cicd-github-actions/
    │   │   ├── README.md                      # PR plan, merge apply, secrets, full YAML
    │   │   ├── examples/
    │   │   │   ├── example-01-basic-plan-workflow/
    │   │   │   ├── example-02-plan-on-pr/
    │   │   │   ├── example-03-apply-on-merge/
    │   │   │   ├── example-04-github-secrets-setup/
    │   │   │   ├── example-05-environment-approvals/
    │   │   │   ├── example-06-matrix-multi-env/
    │   │   │   ├── example-07-plan-comment-on-pr/
    │   │   │   ├── example-08-manual-destroy-workflow/
    │   │   │   ├── example-09-reusable-workflow/
    │   │   │   └── example-10-full-gitops-pipeline/
    │   │   └── .github/
    │   │       └── workflows/
    │   │           ├── terraform-plan.yml
    │   │           └── terraform-apply.yml
    │   ├── 05-terraform-cloud/
    │   │   ├── README.md                      # HCP Terraform, remote runs, VCS integration
    │   │   └── examples/
    │   │       ├── example-01-cloud-block/
    │   │       ├── example-02-remote-execution/
    │   │       ├── example-03-vcs-integration/
    │   │       ├── example-04-variable-sets/
    │   │       ├── example-05-workspace-management/
    │   │       ├── example-06-run-triggers/
    │   │       ├── example-07-private-registry/
    │   │       ├── example-08-team-access/
    │   │       ├── example-09-cost-estimation/
    │   │       └── example-10-terraform-cloud-vs-cicd/
    │   ├── 06-policy-as-code/
    │   │   ├── README.md                      # Sentinel intro, OPA basics, checkov policies
    │   │   └── examples/
    │   │       ├── example-01-what-is-policy-as-code/
    │   │       ├── example-02-checkov-custom-policy/
    │   │       ├── example-03-opa-basics/
    │   │       ├── example-04-opa-terraform-plan/
    │   │       ├── example-05-sentinel-intro/
    │   │       ├── example-06-enforce-tagging-policy/
    │   │       ├── example-07-restrict-resource-types/
    │   │       ├── example-08-cost-policy/
    │   │       ├── example-09-policy-in-ci/
    │   │       └── example-10-policy-best-practices/
    │   ├── 07-drift-detection/
    │   │   ├── README.md                      # Detecting, reporting, and handling drift
    │   │   └── examples/
    │   │       ├── example-01-what-is-drift/
    │   │       ├── example-02-simulate-drift/
    │   │       ├── example-03-terraform-plan-as-drift-check/
    │   │       ├── example-04-terraform-refresh/
    │   │       ├── example-05-scheduled-drift-check/
    │   │       ├── example-06-drift-in-github-actions/
    │   │       ├── example-07-drift-alert-workflow/
    │   │       ├── example-08-ignore-drift-with-lifecycle/
    │   │       ├── example-09-remediate-drift/
    │   │       └── example-10-drift-prevention-strategy/
    │   └── project-06-capstone/               # 🏆 Full Azure stack + CI/CD pipeline
    │
    ├── 📄 .gitignore
    ├── 📄 .terraform-version
    └── 📄 CONVENTIONS.md

---

## 🗺️ Learning roadmap

| # | Phase | Topics | Examples | Project | Status |
|---|-------|--------|----------|---------|--------|
| 1 | 🏗️ Foundations | IaC concepts, install, core workflow, HCL, providers | 10 each | Resource Group | ⬜ Not started |
| 2 | ⚙️ Core config | Variables, outputs, locals, data sources, functions, meta-args, dynamic blocks | 10 each | Storage Account | ⬜ Not started |
| 3 | 💾 State management | Internals, backends, state commands, import, moved blocks, locking | 10 each | Remote backend | ⬜ Not started |
| 4 | 📦 Modules | Basics, writing, composition, registry, versioning, meta-args | 10 each | Web app module | ⬜ Not started |
| 5 | 🔬 Advanced | Workspaces, functions, provisioners, null resource, console, checks, testing | 10 each | Multi-env app | ⬜ Not started |
| 6 | 🚀 Production | Best practices, security, env vars, CI/CD, TF Cloud, policy, drift | 10 each | Full stack capstone | ⬜ Not started |

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
| 📚 **Theory** | Concept explained with real-world analogies, no diagrams |
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
