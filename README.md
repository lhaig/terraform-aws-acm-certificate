# AWS ACM Certificate Terraform Module 

A Terraform module which allows requesting and management of certificates from Amazon Certificate Manager.

This type of resource is supported :
- [ACM - aws_acm_certificate](https://www.terraform.io/docs/providers/aws/r/acm_certificate.html)

# Features

The goal of this module is to give a standard way of generating and managing certificates issued by Amazon.
The module supports :

- Domain Name
- Subject Alternatives Names
- Validation Method
- Tags

## Terraform versions

Module upgraded to terraform 12

## Usage

Certificate Creation example: 

```hcl
module "aws_acm_certificate_tower" {
  source                = "app.terraform.io/<ORG_NAME>/acm-certificate/aws"
  acm_domain_name       = "yourdomain.name"
  acm_san               = ["apps.yourdomain.com","db.yourdomain.com"]
  acm_validation_method = "DNS"
}
```

## Authors

* **Nicolas Ehrman** - *Initial work* - [Hashicorp](https://www.hashicorp.com)

* **Lance Haig** - *Upgraded to terraform 12* - [Hashicorp](https://www.hashicorp.com)
