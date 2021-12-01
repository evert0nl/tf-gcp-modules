Módulo para gerenciamento de instâncias para Google Cloud Platform
---

Example usage:

***main.tf***
```go
module "instances" {
  source = "git@github.com:dihogoteixeira/tf-gcp-modules.git?ref=v1.0"

  amount = 3
  name   = "web-app"
  image  = "centos-cloud/centos-8"
}
```

***outputs.tf***
```go
output "name" {
  value = module.instances.name
}

output "instance_id" {
  value = module.instances.instance_id
}

output "cpu_platform" {
  value = module.instances.cpu_platform
}

output "external_ip" {
  value = module.instances.external_ip
}

output "internal_ip" {
  value = module.instances.internal_ip
}
```
