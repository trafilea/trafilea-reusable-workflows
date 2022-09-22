
# Changelog
All notable changes to this project will be documented on this file

## [2.0.0] - 22/09/2022
### Added
- `terragrunt_deploy_dns.yaml` workflow for deploying Cloudflare DNS Records
- `terragrunt_test_dns.yaml` workflow for test Cloudflare DNS Records


## [1.1.0] - 29/07/2022
### Removed
- TF Var for Datadog API Key on `deploy_terragrunt.yaml` workflow since now we are using it as a secret
- TF Var for Datadog API Key on `terragrunt_test.yaml` workflow since now we are using it as a secret
- Removed PATH input variable on `deploy_terragrunt.yaml` workflow and using ENVIRONMENT input to set the path
- Removed PATH input variable on `terragrunt_test.yaml` workflow and using ENVIRONMENT input to set the path


### Changed
- Docker Image Tag to optional on `terragrunt_test.yaml` workflow since it doesn't impact plan output.
- Job names on `deploy_terragrunt.yaml` workflow
- Job names on `terragrunt_test.yaml` workflow

### Security
- Removed setting AWS Access Keys as environment variables on `deploy_terragrunt.yaml` workflow
- Removed setting AWS Access Keys as environment variables on `terragrunt_test.yaml` workflow


## [1.0.1] - 28/07/2022
### Changed
- `docker_build_and_push.yaml` workflow now sets the tags for the image based on the branch.
- `docker_build_and_push.yaml` workflow now gives two new outputs: **latest_tag** and **image_tag**


## [1.0.0] - 28/07/2022
### Added
- `deploy_terragrunt.yaml` workflow
- `deploy_terraform.yaml` workflow
- `terragrunt_test.yaml` workflow
- `docker_build_and_push.yaml` workflow
- `check_terraform_files.yaml` workflow
#### Note: workflows not mentioned on this version may or may not work.
