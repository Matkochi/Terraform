# Provisionamento de recursos AWS usando Terraform
![terraform](https://github.com/user-attachments/assets/34eede13-7b64-42cf-886b-736886e0c2ce)
![aws](https://github.com/user-attachments/assets/e7c9f676-d4aa-4d02-b07d-896ebf4fe22a)


##### Arquivo main.tf
- Definição do provider: AWS 

- Região: us-east-1(Virgínia)

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
- Criação da VPC
```
resource "aws_vpc" "youtube_vpc" {
  cidr_block = "10.0.0.0/16"
  tags = merge({Name = "youtube-vpc"}, variables.tags)
}
```




