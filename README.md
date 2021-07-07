# Terraform module for Kubernetes Datadog

Deploy datadog for our Kubernetes and Terraform setup. Each code change requires a bump to the version and release so the Terraform registry can get the new changes.

Based off this repo: https://github.com/cookielab/terraform-kubernetes-datadog

Our terraform registry which pulls from this GitHub repo is located here: https://registry.terraform.io/modules/ZZingeroo/datadog/zkubernetes/latest

## Usage

```terraform
provider "kubernetes" {
  # your kubernetes provider config
}

module "datadog" {  
  source  = "ZZingeroo/datadog/zkubernetes"
  version = "1.0.2"

  datadog_agent_api_key = "<API_KEY>"
  datadog_agent_site = "datadoghq.com"
}
```
