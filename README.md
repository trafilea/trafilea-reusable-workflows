# Trafilea Reusable Workflows

## Description
This repo was created in order to generate reusable workflows so we can keep our repos as DRY as possible. 

## Current reusable workflows
* **deploy_terraform**: used to deploy Terraform infrastructure just using Terraform (no Terragrunt or Terraspace)
*  **check_terraform_files**: you can configure some tests to run on your Terraform code when doing a pull request for example. Current checks: _terraform fmt, Checkov, TFSec_

## Wanna contribute?
To contribute to the repo, follow this process:
1. Create a branch for your new reusable workflow.
2. Create the workflow (YAML) file on _.github/workflows_.
3. Send a pull request and let the DevOps/Infra team review it.

