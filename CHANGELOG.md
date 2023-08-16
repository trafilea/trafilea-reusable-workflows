
# Changelog
All notable changes to this project will be documented on this file

## [4.3.0] - 16/08/2023
### Added
- Added `s3-upload-cdn-invalidation.yaml` workflow for uploading static files to S3 and invalidating the CloudFront cache.

## [4.2.0] - 20/06/2023
### Added
- Added `argocd_depoyment.yaml` workflow for commiting to GitOps repo and syncing the ArgoCD App.
- Added `docker_release.yaml` workflow for pushing a Docker image to ECR with a custom tag.

## [4.1.0] - 29/03/2023
### Changed
- Changed `node_lambda_upload.yaml`- Now using 12 DIGITS for Commit SHA instead of 7
- Changed `python_lambda_upload.yaml`- Now using 12 DIGITS for Commit SHA instead of 7

## [4.0.0] - 01/03/2023
### Changed
- Changed `deploy_terragrunt.yaml` - Now checking if the ECR Image exists before making the deploy and sending event to DataDog after a sucessful deploy

## [3.1.2] - 16/01/2023
### Changed
- Changed `python_lambda_upload.yaml` workflow name to _Upload Python Lambda_.
- Changed `node_lambda_upload.yaml` by adding optional input *LAMBDAS_FOLDER*

### Changed
- Changed `python_lambda_upload.yaml` build script in order to correctly build the dependencies into the package

## [3.1.1] - 11/01/2023
### Added
- Added `python_lambda_upload.yaml` workflow for uploading Python Lambdas code to S3.

## [3.1.0] - 17/11/2022
### Added
- Added `node_lambda_upload.yaml` workflow for uploading Nodejs Lambdas code to S3.
- Added `PACKAGE_VERSION` input to `deploy_terragrunt.yaml` workflow.
- Added `PACKAGE_VERSION` input to `terragrunt_test.yaml` workflow.

## [3.0.2] - 10/11/2022
### Added
- `deploy_terragrunt.yaml` now accepts the input: INFRA_PATH, with "terraform" as a default value
- `terragrunt_test.yaml` now accepts the input: INFRA_PATH, with "terraform" as a default value


## [3.0.1] - 20/10/2022
### Changed
- `deploy_terraform.yaml`: Terraform version upgraded to `1.2.9`
- `deploy_terragrunt.yaml`: Terraform version upgraded to `1.2.9`
- `terragrunt_deploy_dns.yaml`: Terraform version upgraded to `1.2.9`
- `terragrunt_test_dns`: Terraform version upgraded to `1.2.9`
- `terragrunt_test`: Terraform version upgraded to `1.2.9`

## [3.0.0] - 19/10/2022
### Changed
- Upgraded AWS-Configure-Credentials and Checkout actions to node16 on all workflows
- `docker_build_and_push.yaml`: removing set-output due to deprecation and future disable

## [2.1.0] - 26/09/2022
### Changed
- `terragrunt_deploy_dns.yaml`: adding CloudFlare API Token secret requirement
- `terragrunt_test_dns.yaml`: adding CloudFlare API Token secret requirement


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
