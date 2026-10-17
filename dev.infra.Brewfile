cask_args appdir: '/Applications', require_sha: true

# Ansible
brew 'ansible' # Automate deployment, configuration, and upgrading | https://www.ansible.com https://github.com/ansible/ansible
brew 'ansible-lint' # Checks ansible playbooks for practices and behaviour | https://docs.ansible.com/projects/lint/ https://github.com/ansible/ansible-lint

# Terraform
# INFO: tenv conflicts with terraform and opentofu (it provides both binaries), install only one of them
brew 'hashicorp/tap/terraform', trusted: true # Tool to build, change, and version infrastructure | https://developer.hashicorp.com/terraform https://github.com/hashicorp/terraform
brew 'opentofu' # Drop-in replacement for Terraform. Infrastructure as Code Tool | https://opentofu.org/ https://github.com/opentofu/opentofu
brew 'tenv' # OpenTofu / Terraform / Terragrunt / Terramate / Atmos version manager | https://tofuutils.github.io/tenv/ https://github.com/tofuutils/tenv
brew 'terraform-docs' # Tool to generate documentation from Terraform modules | https://terraform-docs.io/ https://github.com/terraform-docs/terraform-docs
brew 'infracost' # Cost estimates for Terraform, Terragrunt, and CloudFormation | https://www.infracost.io/docs/ https://github.com/infracost/infracost

# Cloud cli
brew 'awscli' # Official Amazon AWS command-line interface | https://aws.amazon.com/cli/ https://github.com/aws/aws-cli
brew 'aws-vault' # Securely store and access AWS credentials in development environments | https://github.com/ByteNess/aws-vault
cask 'session-manager-plugin' # Plugin for AWS CLI to start and end sessions that connect to managed instances | https://docs.aws.amazon.com/systems-manager/latest/userguide/session-manager-working-with-install-plugin.html
cask 'gcloud-cli' # Set of tools to manage resources and applications hosted on Google Cloud | https://cloud.google.com/cli
brew 'azure-cli' # Microsoft Azure CLI 2.0 | https://learn.microsoft.com/cli/azure/ https://github.com/Azure/azure-cli

# Secrets
brew 'sops' # Editor of encrypted files | https://getsops.io/ https://github.com/getsops/sops
brew 'age' # Simple, modern, secure file encryption | https://age-encryption.org https://github.com/FiloSottile/age

# CI/CD
brew 'act' # Run your GitHub Actions locally | https://nektosact.com https://github.com/nektos/act
brew 'actionlint' # Static checker for GitHub Actions workflow files | https://rhysd.github.io/actionlint/ https://github.com/rhysd/actionlint
