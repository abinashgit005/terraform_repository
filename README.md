# Terraform

### create a terraform block to create a git repo.
```terraform
provider "github" {
    token = "ghp_Ne9Xu2Tpzic7txSxxxxxxxxxxxxxxxxxxxYYYYYYYYYla"
}

resource "github_repository" "terraform_repo" {
  name        = "terraform_repository"
  description = "My awesome terraform repo"
  visibility = "public"
  auto_init = true
}
```

### variables file
To set a lots of variable, we need a variable definations file. Terraform loads automatically the variable defination file if the file name ends with ".tfvars" and ".tfvars.json"
also if the file name ends with ".auto.tfvars" and ".auto.tfvars.json"

### .tfstate file
1. when we create a configuration file to privision our infrastructure, terrafom automatically create a terraform.tfstate file in the local workspace to manage the record. It also determine which part already has been created and which part terraform should create.
2. It records all the resources we have provisioned with terraform in a JSON format with in the terraform.tfstate file as a representation of the real world(here it means the the resources we craeted in the cloud provider).

> [!CAUTION]
> Never delete or manipulate the terraform.tfstae file by yourself.
