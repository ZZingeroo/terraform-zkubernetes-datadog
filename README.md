# Terraform module for Kubernetes Datadog

Deploy datadog for a Kubernetes and Terraform setup

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

  datadog_agent_api_key = "<YOUR_API_KEY>"
  datadog_agent_site = "datadoghq.com"
}
```
