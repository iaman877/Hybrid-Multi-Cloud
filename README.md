# Hybrid-Multi-Cloud

# Getting Started:
1. Clone this repo.
1. Download and install [aws-cli-v2](https://awscli.amazonaws.com/AWSCLIV2.msi) place it somewhere and add the exact path to the `PATH` environment variable.
1. For working with AWS create an `aws cli profile` using `aws configure --profile <newProfileName>` and configure it with `access` and `secret keys`. Terraform will use the profile specified by us in the `.tf` code.
1. I have a profile named `hybrid` created on my system. (The profiles are located in `$HOME/.aws/` by default.)
1. Download and install [`terraform`](https://www.terraform.io/downloads.html) binary extract it somewhere and add the exact path to the `PATH` environment variable.
1. `terraform init` : This will cause terraform to check through your code and download the plugins required for the used providers eg. `terraform-provider-aws` or even `terraform-provider-aws`.
1. `terraform apply --auto-approve` : This starts the infrastructure building process.
1. After done use `terraform destroy --auto-approve` : This starts the infrastructure destroying process.
