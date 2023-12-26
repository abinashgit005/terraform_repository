# terraform_repository

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
