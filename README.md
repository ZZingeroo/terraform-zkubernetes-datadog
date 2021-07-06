# Terraform module for Kubernetes Datadog

Deploy datadog for a Kubernetes and Terraform setup

## Usage

```terraform
provider "kubernetes" {
  # your kubernetes provider config
}

module "datadog" {  
  source  = "ZZingeroo/datadog/kubernetes"
  version = "1.0.0"

  datadog_agent_api_key = "<YOUR_API_KEY>"
  datadog_agent_site = "datadoghq.com" # Set to "datadoghq.eu" to send your Agent data to the Datadog EU site (default: "datadoghq.com")
}
```
