# Hybrid-Multi-Cloud

# Getting Started:
1. Download and install [aws-cli-v2](https://awscli.amazonaws.com/AWSCLIV2.msi)
1. place it somewhere and add the exact path to the `PATH` environment variable..

1. Download and install [`terraform`](https://www.terraform.io/downloads.html) binary extract it  and add the exact path to the `PATH` environment variable.
1. `terraform init` : This will cause terraform to check through your code and download the plugins required for the used providers eg. `terraform-provider-aws` or even `terraform-provider-aws`.
1. `terraform apply --auto-approve` : This starts the infrastructure building process.
1. After done use `terraform destroy --auto-approve` : This starts the infrastructure destroying process.
