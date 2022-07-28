
# Changelog
All notable changes to this project will be documented on this file

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
