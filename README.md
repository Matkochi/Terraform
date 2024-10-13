# Provisionamento de recursos AWS usando Terraform
##### Arquivo main.tf
-Definição do provider: AWS 

-Região: us-east-1(Virgínia)

``` 
terraform {
  required_providers {
    aws = {
      source  = "hashicorp/aws"
      version = "~> 5.0"
    }
  }
}


provider "aws" {
  region = "us-east-1"
  profile = "default"
}
``` 
#### Arquivo vpc.tf 
-Criação da VPC





