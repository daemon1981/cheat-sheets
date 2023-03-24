terraform init
terraform show
terraform plan
terraform apply -auto-approve
terraform destroy

terraform plan -var-file=terraform-myenv.tfvars -out=plan-myenv # show changes required by the current configuration. It looks to the backend file (terraform.tfstate) to evaluate which resources to create
terraform apply plan-myenv # create or update infrastructure (terraform.tfstate)
terraform state rm [ressource.name] # delete a resource from the state
terraform init -backend-config=backend-file.hcl # init with backend file
